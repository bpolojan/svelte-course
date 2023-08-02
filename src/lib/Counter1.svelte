<script>
  let count = 0;

  function increment() {
    count += 1;
  }

  //Reactive statements - each value that we depend on - will make the statement run again if the value changes
  $: {
    if (count > 5) {
      console.log(`Reactive statements - You have clicked ${count} times`);
    }
  }

  let string;
  $: {
    string = `Reactive statements - You have clicked ${count} times`;
  }

  $: someOtherVariable =`Reactive statements - You have clicked ${count} times`; 

</script> 
Reactive statements examples
<button on:click={increment}>Clicks {count}</button>

<h3>"Use the state directly {count} times"</h3>
<h3>{string}</h3>
<h3>{someOtherVariable}</h3>

<style>
  button {
    padding: 15px 20px;
  }
</style>
