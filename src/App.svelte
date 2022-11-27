<script lang="ts">
	import Counter from "./lib/Counter.svelte";
	import Header from "./lib/Header.svelte";
	import ProgressBar from "./lib/ProgressBar.svelte";
</script>

<main
	class="flex flex-col items-center justify-center min-h-screen w-full text-black"
>
	<Header />

	<article class="w-full flex flex-col justify-center items-center w-full">
		<ProgressBar />

		<Counter />
	</article>
</main>

<style>
</style>
