<script>
	import Button from "$lib/Button.svelte";

	let title = "Lorem Ipsum Title";

	const updateTitle = () => {
      console.log("clicked");
		title = "Changed Lorem Ipsum Title";
	};
</script>

<div class="index">
	<h1>{title}</h1>
	<a href="/about">About</a>
	<a href="/users">View Users</a>
	<a href="/products">View Products</a>
	<a href="/counter">Counter App</a>
	<p>
		Lorem ipsum, dolor sit amet consectetur adipisicing elit. Recusandae eaque asperiores cupiditate
		iure, laboriosam modi aliquid accusantium est, facilis alias temporibus ipsum. Sint, ipsam saepe
		atque eum facere inventore quisquam?
	</p>
	<Button buttonType="secondary" on:click={updateTitle}>Change Title</Button>
</div>

<style>
	.index {
		display: block;
		text-align: center;
		margin: 20px;
	}
</style>
