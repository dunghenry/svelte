<script>
  import { Router, Route } from "svelte-routing";
  import About from "./pages/About.svelte";
  import Home from "./pages/Home.svelte";
  import Event from "./pages/Event.svelte";
  export let url = "";
</script>

<Router {url}>
  <div>
    <Route exact path="about"><About /></Route>
    <Route exact path="event"><Event /></Route>
    <Route exact path="/"><Home /></Route>
  </div>
</Router>

<style>
</style>
