<script lang="ts">
	import { register } from 'swiper/element/bundle';
	import img1 from '$lib/img/car0.webp';
	import img2 from '$lib/img/car1.webp';
	import img3 from '$lib/img/car2.webp';

	register();

	const items = [
		{ imageUrl: img1, caption: 'Image 1' },
		{ imageUrl: img2, caption: 'Image 2' },
		{ imageUrl: img3, caption: 'Image 3' }
	];

	const spaceBetween = 10;
	const onProgress = (e: any) => {
		const [swiper, progress] = e.detail;
		console.log(progress);
	};
	const onSlideChange = (e: any) => {
		console.log('slide changed');
	};
</script>

<div class="flex">
	<swiper-container class="relative h-[100vh] min-w-[100vw] flex-1 overflow-hidden">
		{#each items as { imageUrl, caption }}
			<swiper-slide class="h-full">
				<img
					loading="lazy"
					src={imageUrl}
					alt={caption}
					width="100%"
					height="100%"
					class="h-full object-cover"
				/>
			</swiper-slide>
		{/each}
	</swiper-container>

	<!-- <swiper-slide>Slide 2</swiper-slide>
		<swiper-slide>Slide 3</swiper-slide> -->
</div>
