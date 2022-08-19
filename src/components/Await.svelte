<script>
  import axios from "axios";
  const getTodo = async () => {
    const id = Math.floor(Math.random() * 10) + 1;
    try {
      const respone = await axios.get(
        `https://jsonplaceholder.typicode.com/todos/${id}`,
      );
      return respone.data;
    } catch (error) {
      throw new Error(error.message);
    }
  };
  let promise = getTodo();
  const handleClick = () => {
    promise = getTodo();
  };
</script>

<main>
  <button on:click={handleClick}> Get Todo </button>
  <p>{promise}</p>

  {#await promise}
    <p>...Starting</p>
  {:then data}
    <p>{data.title}</p>
  {:catch error}
    <p>{error.message}</p>
  {/await}

  {#await promise then value}
    <p>the value is {value.title}</p>
  {/await}
</main>
