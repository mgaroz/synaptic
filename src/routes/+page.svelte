<script lang="ts">
	import Header from '$lib/components/Header.svelte';
	import Swiper from '$lib/components/Swiper.svelte';
	import Entry from '$lib/components/Entry.svelte';
	import EntryPlain from '$lib/components/EntryPlain.svelte';
	import imageone from '$lib/img/car0.webp';
	import imagetwo from '$lib/img/car1.webp';
</script>

<header class="absolute left-0 right-0 top-6 z-10 mx-auto w-[1160px]">
	<Header />
</header>
<main class="min-h-[100vh] bg-[#1A1924] text-white">
	<Swiper />
	<div id="body" class="mx-2 bg-[#1A1924] pt-28">
		<div class="grid grid-cols-2 gap-2 bg-[#1A1924]">
			<Entry image={imageone} />
			<Entry image={imageone} />
		</div>
		<div class="grid grid-cols-2 gap-2 pt-2">
			<Entry image={imagetwo} />
			<EntryPlain />
		</div>
		<!-- <h1 class="text-3xl font-bold underline">Welcome to SvelteKit</h1>
		<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p> -->
	</div>
</main>
