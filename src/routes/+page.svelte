<script lang="ts">
	import Header from '$lib/components/Header.svelte';
</script>

<header class="absolute left-0 right-0 top-6 mx-auto w-[1160px]">
	<Header />
</header>
<main
	class="min-h-[100vh] bg-[#1A1924] text-white"
	style="background-image: url('https://picsum.photos/id/35/1920/1080')"
>
	<div id="body" class="pt-28">
		<h1 class="text-3xl font-bold underline">Welcome to SvelteKit</h1>
		<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
	</div>
</main>
