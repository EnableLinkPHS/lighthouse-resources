<script>
  import Sidebar from "./Components/Sidebar.svelte";
  import Header from "./Components/Header.svelte";
  import Page from "./Components/Page.svelte";
  import { pageContrast } from "./store.js";
  let page = "home";
</script>
<a id="skip-link" href="#page">Skip to main content</a>
<Sidebar bind:page/>
<Header/>
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
