<script lang="ts">
	import { media } from "$lib/api";
import type { MovieDetails } from "$lib/types";

export let movie:MovieDetails

$:images = movie.images
$:backdrops = images.backdrops.find(backdrop => !backdrop.iso_639_1) || images.backdrops[0]
$:logo = images.logos.find(logo => logo.iso_639_1 === 'en') || images.logos[0]
</script>
<h1 class="text-5xl text-white mt-10 mb-8 font-medium col">
    Today's top movies
</h1>

<a href="/movies/{movie.id}" class="relative col block">
    <img class="w-full aspect-video" src={media(backdrops.file_path,1280)} alt={movie.title} />
    <img class="absolute object-contain left-10 bottom-20 w-4/12 drop-shadow-xl backdrop-filter" src={media(logo.file_path,1280)} alt={movie.title}/>
</a>