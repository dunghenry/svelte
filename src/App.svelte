<script>
  import { Router, Route } from "svelte-routing";
  import About from './pages/About.svelte';
  import Home from './pages/Home.svelte';
  export let url = "";
</script>

<Router url="{url}">
  <div>
    <Route exact path="about"><About/></Route>
    <Route exact path="/"><Home/></Route>
  </div>
</Router>
  
<style>
  
</style>
