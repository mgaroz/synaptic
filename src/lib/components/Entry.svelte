<script lang="ts">
	export let image: any;
</script>

<div class="group relative h-[480px] overflow-hidden">
	<div class="relative h-full w-full overflow-hidden">
		<img
			loading="lazy"
			src={image}
			alt="something"
			class="absolute inset-0 z-0 scale-150 object-cover duration-500 group-hover:scale-100"
		/>
	</div>
	<div class="absolute inset-0 z-10 h-full">
		<div
			class="flex h-fit flex-col justify-end bg-black bg-opacity-0 opacity-0 duration-500 group-hover:bg-opacity-30 group-hover:opacity-100"
		>
			<p>Text one</p>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro optio dolorum facere
				necessitatibus, quibusdam dolorem dicta autem aliquid quo natus ab maxime sequi quia
				repudiandae doloremque tenetur sapiente exercitationem consequuntur.
			</p>
		</div>
	</div>
</div>
