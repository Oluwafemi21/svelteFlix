<script lang="ts">
	import { media } from "$lib/api";
import type { MovieListResult } from "$lib/types";

export let movies:MovieListResult[];


</script>

<div class="carousel flex gap-4 h-80 snap-mandatory overflow-x-scroll scroll-pl-4 col">
    {#each movies as movie}
        <a href="/movies/{movie.id}" class="h-full snap-start aspect-[2/3]">
            <img class="h-full" src={media(movie.poster_path,500)} alt={movie.title} />
        </a>
	{/each}
</div>

<style>
    .carousel::-webkit-scrollbar{
        display: none;
    }
    /* .carousel{
        display:flex;
        height: 10rem;
        gap:1rem;
        scroll-snap-type: mandatory;
        scroll-padding-left: 1rem;
        overflow-x: scroll;
        padding-inline: 1rem;
    } */

    /* a{
        scroll-snap-align: start;
    height: 100%;
    aspect-ratio: 2 / 3;
    }

    img{
        height:100%
    } */

</style>