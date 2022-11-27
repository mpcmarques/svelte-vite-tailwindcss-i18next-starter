<script lang="ts">
	import { onMount } from "svelte";

	let isProgressBarHovered: boolean = false;
	const setIsProgressBarHovered = (value: boolean) => {
		isProgressBarHovered = value;
	};

	let style = `ml-[0px]`;

	onMount(async () => {
		console.log("fired");

		const barWidth = document.querySelector(".loading-bar")?.clientWidth;
		const innerBarWidth =
			document.querySelector(".loading-bar-inner")?.clientWidth;

		setInterval(() => {
			style = `ml-[0px]`;

			setTimeout(() => {
				style = `ml-[${barWidth - innerBarWidth}px]`;

				console.log(style);
			}, 500);

			console.log(style);
		}, 1000);
	});
</script>

<div
	class="loading-bar flex h-10 bg-slate-500 w-full"
	on:mouseenter={() => setIsProgressBarHovered(true)}
	on:mouseleave={() => setIsProgressBarHovered(false)}
>
	<div class="loading-bar-inner h-10 w-20 bg-white {style}">
		{style}
	</div>
</div>

<style>
</style>
