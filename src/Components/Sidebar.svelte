<script>
	import data from '../Assets/data.json';
	import { pageContrast, fontSize } from "../store.js";
	export let page = "home";
	let primary; let text;
	$: switch($pageContrast){
		case "gray": 
			primary = "#5e5e5e"; 
			text = "000000";
			break;
		case "high": 
			primary = "#000000"; 
			text = "ffffff";
			break;
		default: 
			primary = "#2b175f";
			text = "000000";
	}
</script>
<div style="--primary: {primary}; --text: {text}">
	<aside class="Sidebar" role="navigation">
		{#each data.sideitems as item}
			{#if (item.id == page)}
				<button role="link" on:click={() => page = item.id} disabled>{item.name}</button>
			{:else}
				<button role="link" on:click={() => page = item.id}>{item.name}</button>
			{/if}
		{/each}
	</aside>
</div>
<link href='https://fonts.googleapis.com/css?family=Roboto+Slab' rel='stylesheet'>
<style>
	.Sidebar {
		position: fixed;
		top: 15%;
		width: 15%;
		height: 100%;
		padding: 5px;
		background: var(--primary);
	}
	
	.Sidebar button {
		background: none;
		font-family: 'Roboto Slab';
		color: var(--text);
		font-size: 15px;
		text-align: left;
		width: 100%;
		border: none;
		border-radius: 0px;
		border-bottom: 2px solid (--text);
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
