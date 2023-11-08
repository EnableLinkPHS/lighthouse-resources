<script>
  let fontSize = 10;
</script>
<button on:click={e => fontSize++}>+</button>
<button on:click={e => fontSize--}>-</button>
<p style="font-size: {1 + fontSize + 'px'}">Hello.</p>
