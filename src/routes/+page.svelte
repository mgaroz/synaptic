<script lang="ts">
	import Header from '$lib/components/Header.svelte';
	import Carousel from '$lib/components/Carousel.svelte';
</script>

<header class="absolute left-0 right-0 top-6 z-10 mx-auto w-[1160px]">
	<Header />
</header>
<main class="min-h-[100vh] bg-[#1A1924] text-white">
	<Carousel />
	<div id="body" class="pt-28">
		<h1 class="text-3xl font-bold underline">Welcome to SvelteKit</h1>
		<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
	</div>
</main>
