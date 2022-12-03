<script>
	import NestedComp from './NestedComp.svelte';
  let name = "World";
  let src = "/tutorial/image.gif";
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