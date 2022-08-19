<script>
    let string = `this string contains some <strong>HTML!!!</strong>`;
    let count = 0;
    const imcrementCount = () =>{
        count += 1;
        $: {
            console.log(count);
        }
    }
    $: doubled = count * 2;

    $: if (count >= 10) {   
        alert('count is dangerously high!');
        count = 9; // set count and break
    }
</script>

<main>
    <h1>Hello Component</h1>
    <p>{@html string}</p>
    <p>{count}</p>
    <p>{doubled}</p>
    <button on:click={imcrementCount}>Increment</button>
</main>
  
<style>
  
</style>
