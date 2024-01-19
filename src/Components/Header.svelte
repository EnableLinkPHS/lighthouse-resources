<script>
	import { pageContrast, fontSize, underline } from "../store.js";
	const changeContrast = (value) => $pageContrast != value ? value : "none";
	let primary;
	$: switch($pageContrast){
		case "gray": 
			primary = "#5e5e5e";
			break;
		case "high": 
			primary = "#000000";
			break;
		default: 
			primary = "#2b175f";
	}
</script>
<div class="Header" style="--primary: {primary}" role="toolbar">
	<button on:click={() => $fontSize = Math.min(30, $fontSize + 1)}>Increase Font</button>
	<button on:click={() => $fontSize = Math.max(5, $fontSize - 1)}>Decrease Font</button>
	<button on:click={() => $pageContrast = changeContrast("gray")}>Grayscale</button>
	<button on:click={() => $pageContrast = changeContrast("high")}>High Contrast</button>
	<button on:click={() => $underline = !($underline)}>URL Underline</button>
</div>
<style>
	.Header {
		position: fixed;
		width: 100%;
	}

	.Header button {
		padding: 1%;
		width: 20%;
		float: left;
		background-color: var(--primary);
		color: white;
		border: none;
		font-family: 'Roboto Slab';
		font-size: 15px;
		text-align: center;
		display: block;
	}
	.Header button:hover {
		background-color: white;
		color: #000000;
	}
</style>