<script>

	import Nav from './comps/sections/Nav.svelte';
	import Hero from './comps/sections/Hero.svelte';
	import About from './comps/sections/About.svelte';
	import Career from './comps/sections/Career.svelte';
	import Projects from './comps/sections/Projects.svelte';
	import Contact from './comps/sections/Contact.svelte';
	let y = 0;
	let innerWidth = 0;
</script>

<main>
	<Nav y={y} />
	<Hero />
	<About y={y} innerWidth={innerWidth}/>
	<Career innerWidth={innerWidth}/>
	<Projects y={y} innerWidth={innerWidth}/>
</main>

<svelte:window bind:scrollY={y} bind:innerWidth={innerWidth}/>

<style>
	main {
		height: 10000px;
	}
</style>