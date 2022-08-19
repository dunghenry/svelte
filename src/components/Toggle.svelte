<script>
  let user = { loggedIn: false };
  const toggle = () => {
    user.loggedIn = !user.loggedIn;
  };
  const x = 7;
</script>

<main>
  {#if user.loggedIn}
    <button on:click={toggle}>Logout</button>
  {/if}
  {#if !user.loggedIn}
    <button on:click={toggle}>Login</button>
  {/if}
  {#if user.loggedIn}
    <button on:click={toggle}>Logout</button>
  {:else}
    <button on:click={toggle}>Login</button>
  {/if}

  {#if x > 7}
    <p>{x} is greater than 10</p>
  {:else if x < 5}
    <p>{x} is less than 5</p>
  {:else}
    <p>{x} between 5 and 10</p>
  {/if}
</main>
