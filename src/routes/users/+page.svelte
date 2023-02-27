<script>
	import { onMount } from "svelte";
	import axios from "axios";

	let users = [];

	onMount(async () => {
		try {
			const { data } = await axios.get("https://dummyjson.com/users");
			users = data.users;
		} catch (err) {
			console.log(err);
		}
	});
</script>

<a href="/">Home</a>
<div class="guides">
	<h1>Users</h1>
	<ul>
		{#each users as user}
			<li>
				<a href="/">{user.username}</a>
			</li>
		{/each}
	</ul>
</div>

<style>
	.guides {
		margin-top: 20px;
	}
	ul {
		list-style-type: none;
		padding: 0;
	}
	a {
		display: inline-block;
		margin-top: 10px;
		padding: 10px;
		border: 1px dotted rgba(255, 255, 255, 0.2);
	}
</style>
