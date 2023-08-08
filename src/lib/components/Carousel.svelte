<script lang="ts">
	import emblaCarouselSvelte, { type EmblaCarouselType } from 'embla-carousel-svelte';
	import Autoplay from 'embla-carousel-autoplay';
	import img1 from '$lib/img/car0.webp';
	import img2 from '$lib/img/car1.webp';
	import img3 from '$lib/img/car2.webp';

	const items = [
		{ imageUrl: img1, caption: 'Image 1' },
		{ imageUrl: img2, caption: 'Image 2' },
		{ imageUrl: img3, caption: 'Image 3' }
	];

	let emblaApi;

	const options = {
		slidesToSroll: 1,
		loop: true
	};

	const autoplayOptions = {
		delay: 4000
	};

	let plugins = [Autoplay(autoplayOptions)];

	const onInit = (event: CustomEvent<EmblaCarouselType>) => {
		emblaApi = event.detail;
	};
</script>

<section class="relative -z-0">
	<div class="embla" use:emblaCarouselSvelte={{ options, plugins }} on:emblaInit={onInit}>
		<div class="embla__container">
			{#each items as { imageUrl, caption }}
				<div class="embla__slide">
					<img loading="lazy" src={imageUrl} alt={caption} width="100%" height="100%" />
					<div class="embla__button embla__button--prev flex items-start">
						<h1 class="text-4xl">Hello</h1>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<style>
	.embla {
		overflow: hidden;
	}

	.embla__container {
		display: flex;
	}

	.embla__slide {
		overflow: hidden;
		flex: 1;
		min-width: 100vw;
		position: relative;
		height: 100vh;
	}

	.embla__slide img {
		transition: transform 0.75s cubic-bezier(0.165, 0.84, 0.44, 1);
		object-fit: cover;
		height: 100%;
		width: 100%;
	}

	.embla__button {
		z-index: 50;
		color: #fff;
		position: absolute;
		display: flex;
		align-items: center;
		justify-content: center;
		top: 50%;
		width: 1160px;
		/* transform: translateY(-50%); */
		/* cursor: pointer; */
		/* width: 3rem;
		height: 3rem; */
		/* border-radius: 50%; */
		/* background-color: rgba(255, 255, 255, 0.7); */
		transition: background-color 0.2s cubic-bezier(0.165, 0.84, 0.44, 1);
	}

	.embla__button--prev {
		left: 1.6rem;
	}
</style>
