<script lang="ts">
	import Header from '$lib/components/Header.svelte';
	import Swiper from '$lib/components/Swiper.svelte';
	import Entry from '$lib/components/Entry.svelte';
	import EntryPlain from '$lib/components/EntryPlain.svelte';
	import imageone from '$lib/img/car0.webp';
	import imagetwo from '$lib/img/car1.webp';
	import imagethree from '$lib/img/car2.webp';

	let lengths = ['50%_50%', '25%_25%_50%', '33%_33%_33%', '30%_30%_40%', '50%_25%_25%'];
</script>

<header class="absolute left-0 right-0 top-6 z-10 mx-auto w-[1160px]">
	<Header />
</header>
<main class="min-h-[100vh] bg-[#1A1924] text-white">
	<Swiper />
	<div id="body" class="mx-2 bg-[#1A1924] pt-28">
		<!-- <div class="grid grid-cols-2 gap-2 bg-[#1A1924]">
			<Entry image={imageone} />
			<Entry image={imageone} />
		</div>
		<div class="grid grid-cols-3 gap-2 pt-2">
			<Entry image={imagetwo} />
			<Entry image={imagethree} />
			<EntryPlain />
		</div>
		<div class="grid grid-cols-[28%_28%_44%] gap-2 pt-2">
			<Entry image={imageone} />
			<Entry image={imagethree} />
			<Entry image={imagetwo} />
		</div> -->
		<div class="flex flex-wrap gap-2">
			<Entry image={imageone} />
			<Entry image={imagetwo} />
			<Entry image={imagethree} />
			<Entry image={imageone} />
			<Entry image={imagetwo} />
			<Entry image={imagethree} />
			<Entry image={imageone} />
			<Entry image={imagetwo} />
			<EntryPlain />
		</div>
	</div>
</main>
