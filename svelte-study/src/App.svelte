<script>
	import NestedComp from './NestedComp.svelte';
  let name = "World";
  let src = "/tutorial/image.gif";
  let string = 'this string contains <i>HTML tag</i>'
  let count = 0;

  $: doubled = count * 2;

  function incCount(){
	count += 1;
  }
</script>

<style>
	p {
		color: purple;
		font-family: 'Comic Sans MS', cursive;
		font-size: 1em;
	}
</style>

<h1>Hello, {name}!</h1>

<img {src} alt="Dancing man" />

<p>Paragraph</p>

<NestedComp />

<p>{@html string}</p>

<button on:click={incCount}>
	Clicked {count} {count === 1 ? 'Time' : 'Times'}
</button>

<p>{count} doubled is {doubled}</p>