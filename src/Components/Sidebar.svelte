<script context="module">
	import data from '../Assets/data.json';
</script>
<aside class="Sidebar">
	{#each data.sideitems as item}
		<button>{item.id}</button>
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
		border: none;
		font-family: 'Roboto Slab';
		padding: 6px;
		padding-top: 5%;
		padding-bottom: 5%;
		border-bottom: 2px solid white;
		text-align: left;
		margin: 0px;
		font-size: 15px;
		color: white;
		overflow: auto;
		width: 100%;
		cursor: pointer;
		text-decoration: underline;
	}

	.Sidebar button:last-child {
		border-bottom: 0px;
	}
</style>
