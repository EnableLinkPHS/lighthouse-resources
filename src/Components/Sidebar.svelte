<script>
	import data from '../Assets/data.json';
	export let page = "home";
	export let contrast = "none";
	let primary = "#2b175f";
	let text = "ffffff";
	function setCurrent(value){ page = value; }
</script>
<aside class="Sidebar" role="navigation">
	{#each data.sideitems as item}
		{#if (item.id == page)}
			<button role="link" on:click={() => setCurrent(item.id)} disabled>{item.name}</button>
		{:else}
			<button role="link" on:click={() => setCurrent(item.id)}>{item.name}</button>
		{/if}
	{/each}
</aside>
<link href='https://fonts.googleapis.com/css?family=Roboto Slab' rel='stylesheet'>
<style>
	.Sidebar {
		position: fixed;
		top: 20%;
		width: 20%;
		height: 100%;
		padding: 5px;
		background: #2b175f;
	}
	
	.Sidebar button {
		background: none;
		font-family: 'Roboto Slab';
		color: white;
		font-size: 15px;
		text-align: left;
		width: 100%;
		border: none;
		border-radius: 0px;
		border-bottom: 2px solid white;
		margin: 0px;
		padding: 6px;
		padding-top: 5%;
		padding-bottom: 5%;
		overflow: auto;
		cursor: pointer;
		text-decoration: underline;
	}

	.Sidebar button:hover {
		background-color: white;
		color: black;
	}

	.Sidebar button[disabled] {
		background : white!important;
		color: black;
	}

	.Sidebar button:last-child {
		border-bottom: 0px;
	}
</style>
