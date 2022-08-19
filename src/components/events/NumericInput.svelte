<script>
  let a = 1;
  let b = 2;
</script>

<main>
  <label>
    <input type="number" max="10" min="0" bind:value={a} />
    <input type="range" min="0" max="10" bind:value={a} />
  </label>
  <label>
    <input type="number" max="10" min="0" bind:value={b} />
    <input type="range" min="0" max="10" bind:value={b} />
  </label>
  <p>{a} + {b} = {a + b}</p>
</main>

<style>
  label {
    display: flex;
  }
  input,
  p {
    margin: 6px;
  }
</style>
