<script>
  export let name;
  const emojis = {
    apple: "🍎",
    banana: "🍌",
    carrot: "🥕",
  };
  const emoji = emojis[name];
</script>

<main>
  <p>
    <span>The emoji for {name} is {emoji}</span>
  </p>
</main>
