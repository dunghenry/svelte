<script>
import Hello from "../components/Hello.svelte";
import Info from "../components/Info.svelte";
import Props from "../components/Props.svelte";
import Updating from "../components/Updating.svelte";
const pkg = {
    name: "Svelte",
    version: 3,
    speed: 'blazing',
    website: 'https://svelte.dev'
}
</script>

<main>
    <h1>Home Page</h1>
    <Hello/>
    <Updating/>
    <Props answer={42}/>
    <Props/>
    <Info {...pkg} />
    <Info name={pkg.name} version={pkg.version} speed={pkg.speed} website={pkg.website}/>
</main>
  
<style>
  
</style>
