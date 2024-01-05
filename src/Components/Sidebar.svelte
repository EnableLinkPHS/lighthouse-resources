<script context="module">
	import data from '../Assets/data.json';
</script>
<aside class="Sidebar" role="navigation">
	{#each data.sideitems as item}
		<button role="link">{item.name}</button>
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
		background: none!important;
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

	.Sidebar button:last-child {
		border-bottom: 0px;
	}
</style>
