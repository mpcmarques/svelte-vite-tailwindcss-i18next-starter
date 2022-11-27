<script lang="ts">
	let count: number = 0;
	const increment = () => {
		count += 1;
	};
</script>

<button on:click={increment} class="counter my-4">
	count is {count}
</button>

<style>
	.counter {
		border-radius: 10rem;
		border: 2px solid black;
		width: 200px;
	}

	.counter:hover {
		box-shadow: 10px 5px 5px 5px black;
	}
</style>
