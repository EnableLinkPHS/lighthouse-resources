<script>
  let fontSize = 10;
</script>
<button on:click={e => fontSize++} aria-label="foo">+</button>
<button on:click={e => fontSize--} aria-label="bar">-</button>
<p style="font-size: {1 + fontSize + 'px'}">Hello.</p>
