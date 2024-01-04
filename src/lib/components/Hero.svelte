<script lang="ts">
	import { media } from "$lib/api";
import type { MovieDetails } from "$lib/types";

export let movie:MovieDetails

$: images = movie.images
$:backdrops = images.backdrops[1]
</script>

<a href="/movie/{movie.id}">
    <img src={media(backdrops.file_path,1280)} alt={movie.title} />
</a>