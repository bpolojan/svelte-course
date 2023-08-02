<script>
  let counter1 = 0;
  let counter2 = 0;
  function increment1() {
    counter1 += 1;
  }

  function increment2() {
    counter2 += 1;
  }

  function getTotal() {
    return counter1 + counter2;
  }

  function getTotalParams(x,y) {
    return x + y;
  }

  //This is not going to work - In reactive statement - the States you are depending on musst appear in the Reactive structure
  $: totalCount  = `Svelte will not know that this funtion depends in count1 and count2 -  ${getTotal()}`;

  // This will work - because of Reactive Statements
  $: totalCount2 = `Count1 and Count 2 appear in the string   you have clicked ${counter1+counter2}`;

  $: totalCount3= `Count1 and Count 2 appear as parameters ${getTotalParams(counter1, counter2)}`;
</script>
Reactive statements behavior
Counter
<button on:click={increment1}>Clicks1 {counter1}</button>
<button on:click={increment2}>Clicks2 {counter2}</button>

<h3>{totalCount}</h3>
<h3>{totalCount2}</h3>
<h3>{totalCount3}</h3>

<style>
  button {
    padding: 15px 20px;
  }
</style>
