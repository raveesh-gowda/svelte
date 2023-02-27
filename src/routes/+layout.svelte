<script>
	import Title from "$lib/Title.svelte";

	import "../assets/styles/global.css"

	let year = new Date().getFullYear();
</script>

<header>
	<Title title="App Title" />
</header>
<main>
	<slot />
</main>
<footer>
	<p>Copyright &copy {year} Svelte Demo</p>
</footer>

<style>
	header {
		display: flex;
	}
	main {
		max-width: 960px;
		margin: 20px auto;
	}
	footer {
		text-align: center;	
	}
</style>
