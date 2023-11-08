<script>
  let fontSize = 0;
</script>
<button on:click={e => fontSize++} label="Increase font size">+</button>
<button on:click={e => fontSize = Math.max(0, fontSize - 1)} label="Decrease font size">-</button>
<p style="font-size: {10 + fontSize + 'px'}">Hello.</p>
