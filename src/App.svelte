<script>
  let name = 'Svelte';
  let src='https://upload.wikimedia.org/wikipedia/commons/a/a2/Iasi_judetul_Iasi.jpg' ;
  let string = 'Some <strong>String</strong> with html'
  
  import Counter from './lib/Counter1.svelte';
</script>

<h1> Hello {name.toUpperCase()}!</h1> 
<p>{@html string}</p>
<img src={src} alt ="Some text {name}" width="500" height="300">
<p></p>

<Counter /> 

<style>
  h1 {
    color: red;
  } 
</style>