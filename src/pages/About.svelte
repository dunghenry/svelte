<script>
  import Await from "../components/Await.svelte";
  import Cats from "../components/Cats.svelte";
  import DomEvent from "../components/DomEvent.svelte";
  import Fruits from "../components/Fruits.svelte";
  import Toggle from "../components/Toggle.svelte";
  let fruits = [
    { id: 1, name: "apple" },
    { id: 2, name: "banana" },
    { id: 3, name: "carrot" },
  ];
  const handleDeleteFruit = () =>{
    fruits = fruits.splice(1);
  }
  const handleDispatch = (e) =>{
    console.log(e.detail)
    alert(e.detail.textContent);
  }
</script>

<main>
  <h1>About Page</h1>
  <Toggle />
  <Cats />
  <button on:click={handleDeleteFruit}>Remove first fruit</button>
  {#each fruits as fruit (fruit.id)}
    <Fruits name={fruit.name} />
  {/each}
  <Await/>

  <DomEvent on:message={handleDispatch}/>
</main>

<style>
</style>
