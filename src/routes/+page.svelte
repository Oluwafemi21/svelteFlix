<script lang="ts">
    import Hero from '$lib/components/Hero.svelte'
	export let data;
    console.log(data.featured)
</script>

<Hero movie={data.featured}/>
<section>
    <div>
        <h3 class="text-white text-2xl">Trending</h3> <span class="text-netflix underline">see all</span>
    </div>
    <div>
        
    </div>

</section>