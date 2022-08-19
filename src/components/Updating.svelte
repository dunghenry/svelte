<script>
    let numbers = [1, 2, 3, 4];

    // const addNumber = () =>{
    //     numbers.push(numbers.length + 1);
    //     numbers = numbers;
    // }

    // const addNumber = () =>{
    //     numbers = [...numbers, numbers.length + 1];
    // }

    const addNumber = () =>{
        numbers[numbers.length] = numbers.length + 1;
    }
    
    $: sum = numbers.reduce((item, total) => item + total);
</script>

<main>
    <h1>Updaing Component</h1>
    <p>{sum}</p>
    <button on:click={addNumber}>Add a number</button>
</main>

<style>

</style>