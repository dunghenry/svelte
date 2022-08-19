<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();
  let m = { x: 0, y: 0 };
  const handleMousemove = (event) => {
    m.x = event.clientX;
    m.y = event.clientY;
  };
  const handleClick = () => {
    alert("Click me!");
  };

  const handleDispatch = () => {
    dispatch('message', {
        textContent: "Hello world!"
    })
  };
</script>

<div on:mousemove={handleMousemove}>
  The mouse position is {m.x} x {m.y}
</div>
<!-- inline -->
<div on:mousemove={(e) => (m = { x: e.clientX, y: e.clientY })}>
  The mouse position is {m.x} x {m.y}
</div>
<button on:click|once={handleClick}> Click me! </button>
<button on:click={handleDispatch}>Dispatch event component parent</button>

<style>
  div {
    width: 100%;
    height: 100%;
  }
</style>
