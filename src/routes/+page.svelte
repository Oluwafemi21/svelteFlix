<script lang="ts">
    import Carousel from '$lib/components/Carousel.svelte';
import Hero from '$lib/components/Hero.svelte'
	export let data;
</script>

<Hero movie={data.featured}/>
<section>
    <div class="mt-10 mb-8 col">
        <h3 class="text-white text-4xl">Trending 
            <a href="/movies/trending" class="ml-2 text-netflix underline text-3xl">see all</a>
        </h3>
    </div>
    <Carousel movies={data.trending.results} /> 
    </section>
<section>
    <div class="mt-10 mb-8 col">
        <h3 class="text-white text-4xl">Now playing 
            <a href="/movies/now_playing" class="ml-2 text-netflix underline text-3xl">see all</a>
        </h3> 
    </div>
    <Carousel movies={data.now_playing.results} /> 

    </section>
<section>
    <div class="mt-10 mb-8 col">
        <h3 class="text-white text-4xl">Upcoming
            <a href="/movies/upcoming" class="ml-2 text-netflix underline text-3xl">see all</a>
        </h3> 
    </div>
    <Carousel movies={data.upcoming.results} /> 


</section>