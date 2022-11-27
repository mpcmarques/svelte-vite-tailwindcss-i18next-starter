<script lang="ts">
	let count: number = 0;
	const increment = () => {
		count += 1;
	};
</script>

<button
	on:click={increment}
	class="counter bg-slate-400  text-slate-200 my-4 shadow-md hover:bg-slate-300 rounded-md p-2"
>
	count is {count}
</button>

<style>
</style>
