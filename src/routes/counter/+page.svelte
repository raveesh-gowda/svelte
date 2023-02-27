<script>
	import Button from "../../lib/Button.svelte";

	let count = 0;

	const decrement = () => {
		count -= 1;
	};

	const reset = () => {
		count = 0;
	};

	const increment = () => {
		count += 1;
	};
</script>

<a href="/">Home</a>

<div class="counter">
	<h3>Counter - {count}</h3>
	<Button buttonType="primary" on:click={decrement}>-</Button>
	<Button buttonType="primary" inverse on:click={reset}>0</Button>
	<Button buttonType="secondary" on:click={increment}>+</Button>
</div>

<style>
	.counter {
		text-align: center;
		margin: 100px;
	}
	h3 {
		font-size: large;
		font-weight: bold;
	}
</style>
