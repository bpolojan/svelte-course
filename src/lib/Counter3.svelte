<script>
  let counter1 = 0;
  let counter2 = 0;

  function setCount2(x) {
    counter2 = x;
  }

  //The order of reactive statements in important - The statement that updates count2 should be above. 
  $: setCount2(counter1); // this reactive statement will run each time count1 is changed and Count 2 will update
  $: count2Value = `Count 2 is ${counter2}`; // When count2 is updated we expect that string will be updated - because string depends on count 2

  function increment1() {
    counter1 += 1;
  }
</script>

Reactive statements behavior
<button on:click={increment1}>Clicks1 {counter1}</button>
<h3>{count2Value}</h3>
<style>
  button {
    padding: 15px 20px;
  }
</style>
