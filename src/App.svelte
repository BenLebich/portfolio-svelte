<script>

	import Nav from './comps/sections/Nav.svelte';
	import Hero from './comps/sections/Hero.svelte';
	import About from './comps/sections/About.svelte';
	import Career from './comps/sections/Career.svelte';
	import Projects from './comps/sections/Projects.svelte';
	import Contact from './comps/sections/Contact.svelte';
	import Social from './comps/sections/Social.svelte';
	import Footer from './comps/sections/Footer.svelte';
	
	let y = 0;
	let innerWidth = 0;
</script>

<main>
	<Nav y={y} innerWidth={innerWidth}/>
	<Hero />
	<About y={y} innerWidth={innerWidth}/>
	<Career innerWidth={innerWidth}/>
	<Projects y={y} innerWidth={innerWidth}/>
	<Contact y={y} innerWidth={innerWidth}/>
	<Social />
	<Footer />
</main>

<svelte:window bind:scrollY={y} bind:innerWidth={innerWidth}/>

<style>

</style>