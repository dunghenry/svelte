<script>
import CustomButton from "../components/events/CustomButton.svelte";
import NumericInput from "../components/events/NumericInput.svelte";

  import Outer from "../components/events/Outer.svelte";
import TextInput from "../components/events/TextInput.svelte";
  function handleMessage(event) {
    alert(event.detail.text);
  }

  function handleClick() {
    alert("Button Clicked");
  }
</script>

<main>
  <h1>Event Page</h1>
  <Outer on:message={handleMessage} />
  <CustomButton on:click={handleClick} />
  <TextInput />
  <NumericInput/>
</main>
