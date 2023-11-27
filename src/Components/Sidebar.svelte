<aside class="Sidebar">
	{#each sideitems as item}
		<p>{item}</p>
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
	    background: #2b175f
	}
	
	.Sidebar p {
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
	}

	.Sidebar p:last-child {
		border-bottom: 0px;
	}
</style>
<script>
	let sideitems = ["Supply Stores",
					"Vocational Rehab",
					"Transportation",
					"MD DORS",
					"DeafBlind Services",
					"Housing",
					"Mobile Apps"];
</script>