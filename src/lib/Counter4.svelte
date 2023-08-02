<script>
  //Component properties
  export let initialCount;
  export let maxCount = undefined; //optional parameters. Will be overwritten if they receive a value  

  let counter1 = initialCount;

  function increment() {
    if(counter1===maxCount) return;
    counter1 += 1;
  }

  //$$props = property of component
  //$$restProps = property of component which are not exported
  console.log($$props, $$restProps)
</script>

<button on:click={increment}>Clicks count {counter1}</button>

<style>
  button {
    padding: 15px 20px;
  }
</style>