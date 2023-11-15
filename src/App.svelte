<script>
  let fontSize = 0;
  import { Sidebar } from "./Components/Sidebar.svelte";
</script>
<button on:click={e => fontSize = Math.min(60, fontSize + 1)} aria-label="Increase font size">+</button>
<button on:click={e => fontSize = Math.max(-3, fontSize - 1)} aria-label="Decrease font size">-</button>
<p style="font-size: {10 + fontSize + 'px'}">Hello.</p>
<Sidebar/>
