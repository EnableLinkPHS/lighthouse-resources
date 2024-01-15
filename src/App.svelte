<script>
  let fontSize = 0;
  import Sidebar from "./Components/Sidebar.svelte";
  import Header from "./Components/Header.svelte";
  import Page from "./Components/Page.svelte";
  import { pageID, pageContrast} from "./store.js";
  let page = "home";
</script>
<!--button on:click={e => fontSize = Math.min(60, fontSize + 1)} aria-label="Increase font size">+</button>
<button on:click={e => fontSize = Math.max(-3, fontSize - 1)} aria-label="Decrease font size">-</button>
<p style="font-size: {10 + fontSize + 'px'}">Hello.</p-->
<a id="skip-link" href="#page">Skip to main content</a>
<Sidebar bind:page contrast={$pageContrast}/>
<Header/>
<Page current={page}/>
<style>
  #skip-link {
    position: absolute;
    left: 50%;
    transform: translateY(-100%);
  }
</style>