<script>
  let name = 'Svelte';
  let src='https://upload.wikimedia.org/wikipedia/commons/a/a2/Iasi_judetul_Iasi.jpg' ;
  let string = 'Some <strong>String</strong> with html'
  
  import Counter from './lib/Counter4.svelte';

  const maxCount=6;

  const props = {
    maxCount:10,
    initialCount:2
  }
</script>
<h3>Component Properties</h3>

<p>Initial count is set to 3, max count is set as undefined in component</p>
<Counter initialCount={3} /> 
<p>Initial count is set to 3, max count is set to 10 - overwrite default undefined value</p>
 <Counter initialCount={3} maxCount={10}/>  
<p>Initial count is set to 4, max count is set to 6 in component</p>
<Counter initialCount={4} maxCount={maxCount}/> 
<p>Properties are declared in a variable. In console you can also check the values of $$props, $$restProps</p>
<Counter {...props} x="y"/> 

<style>
  h1 {
    color: red;
  } 
</style>