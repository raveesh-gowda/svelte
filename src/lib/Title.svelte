<script>
	import logo from "../assets/images/logo.png";

	export let title = "App Title";
</script>

<div class="title">
	<img src={logo} alt="Demo App" />
	<h1>{title}</h1>
</div>

<style>
	.title {
		display: flex;
	}
	.title img {
		display: inline-block;
		margin: 15px;
		width: 75px;
		height: 50px;
		filter: invert(88%) sepia(18%) saturate(886%) hue-rotate(199deg) brightness(100%) contrast(90%);
	}
	.title h1 {
		margin-left: 10px;
	}
</style>
