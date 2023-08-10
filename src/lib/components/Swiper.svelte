<script lang="ts">
	import { register } from 'swiper/element/bundle';

	register();

	const spaceBetween = 10;
	const onProgress = (e: any) => {
		const [swiper, progress] = e.detail;
		console.log(progress);
	};
	const onSlideChange = (e: any) => {
		console.log('slide changed');
	};
</script>

<swiper-container
	slides-per-view={1}
	space-between={spaceBetween}
	centered-slides={true}
	pagination={{
		hideOnClick: true
	}}
	breakpoints={{
		768: {
			slidesPerView: 1
		}
	}}
	on:progress={onProgress}
	on:slidechange={onSlideChange}
>
	<swiper-slide>Slide 1</swiper-slide>
	<swiper-slide>Slide 2</swiper-slide>
	<swiper-slide>Slide 3</swiper-slide>
</swiper-container>
