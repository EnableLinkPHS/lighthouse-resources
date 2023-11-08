<script>
  let fontSize = 10;
</script>
<button on:click={e => fontSize++} id="foo">+</button>
<button on:click={e => fontSize--} id="bar">-</button>
<p style="font-size: {1 + fontSize + 'px'}">Hello!</p>
