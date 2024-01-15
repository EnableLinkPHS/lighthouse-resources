<script>
	export let contrast = "none";
	export let fontSize = 10;
	export let underline = false;
	function changeContrast(value){
		contrast != value ? contrast = value : contrast = "none";
	}
</script>
<div class="Header" role="toolbar">
	<button on:click={() => fontSize = Math.min(60, fontSize + 1)}>Increase Font</button>
	<button on:click={() => fontSize = Math.max(5, fontSize - 1)}>Decrease Font</button>
	<button on:click={() => changeContrast("gray")}>Grayscale</button>
	<button on:click={() => changeContrast("high")}>High Contrast</button>
	<button on:click={() => underline = !underline}>URL Underline</button>
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
		background-color: #2b175f;
		color: white;
		border: none;
		font-family: 'Roboto Slab';
		font-size: 15px;
		text-align: center;
		display: block;
	}
	.Header button:hover {
		background-color: #eeeeee;
		color: #000000;
	}
</style>