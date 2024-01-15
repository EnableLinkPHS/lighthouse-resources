<script>
  import Sidebar from "./Components/Sidebar.svelte";
  import Header from "./Components/Header.svelte";
  import Page from "./Components/Page.svelte";
  //import { pageID, pageContrast} from "./store.js";
  let page = "home"; let contrast = "none"; let fontSize = 10; let underline = false;
</script>
<!--button on:click={e => fontSize = Math.min(60, fontSize + 1)} aria-label="Increase font size">+</button>
<button on:click={e => fontSize = Math.max(-3, fontSize - 1)} aria-label="Decrease font size">-</button>
<p style="font-size: {10 + fontSize + 'px'}">Hello.</p-->
<a id="skip-link" href="#page">Skip to main content</a>
<Sidebar bind:page contrast={contrast}/>
<Header bind:contrast bind:fontSize bind:underline/>
<Page current={page}/>
<style>
  #skip-link {
    position: absolute;
    left: 0%;
    transform: translateY(-100%);
  }

  #skip-link:focus {
    transform: translateY(0%);
  }
</style>