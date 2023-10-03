<script lang="ts">
	export let image: any;
	let ws = ['50%', '25%', '33%'];
	let random = Math.floor(Math.random() * ws.length);
	let lengths = [
		'w-[50%_50%]',
		'w-[25%_25%_50%]',
		'w-[33%_33%_33%]',
		'w-[30%_30%_40%]',
		'w-[50%_25%_25%]'
	];
	let eles = ['w-1/2', 'w-1/3', 'w-1/4'];
	// let possibleWidths = [25, 33, 50];

	// function calc(width: number) {
	// 	let currentWidth = width;
	// 	let accumulatedWidth = 0;

	// 	if (accumulatedWidth + currentWidth !== 100) {
	// 		accumulatedWidth = accumulatedWidth + currentWidth;
	// 	}
	// }
</script>

<!-- Need to randomize width on each iteration every time! for real!!! -->

<div class="group relative overflow-hidden md:h-[600px] {eles[random]} flex-1 basis-1/4">
	<div class="relative h-full w-full overflow-hidden">
		<img
			loading="lazy"
			src={image}
			alt="something"
			class="absolute inset-0 z-0 h-full scale-150 object-cover duration-500 group-hover:scale-100"
		/>
	</div>
	<div class="absolute inset-0 z-10 h-full">
		<div
			class="flex h-full flex-col justify-end bg-gradient-to-b from-transparent to-black p-2 opacity-0 duration-500 group-hover:bg-opacity-30 group-hover:opacity-100"
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

<!-- save previous width in a variable and then deduce that from 100 to pick the next value making sure it doesn't exceed 100 -->
