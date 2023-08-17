<script lang="ts">
	export let image: any;
</script>

<div class="relative h-full">
	<img
		loading="lazy"
		src={image}
		alt="something"
		class="absolute left-0 right-0 z-0 object-cover"
	/>
	<div
		class="absolute bottom-0 left-0 z-10 flex h-full flex-col justify-end opacity-0 hover:opacity-100"
	>
		<p>Text one</p>
		<p>
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro optio dolorum facere
			necessitatibus, quibusdam dolorem dicta autem aliquid quo natus ab maxime sequi quia
			repudiandae doloremque tenetur sapiente exercitationem consequuntur.
		</p>
	</div>
</div>
