<script>
import NestedComp from './NestedComp.svelte';
import Nested1 from './Nested1.svelte';
import Information from './Information.svelte';
import IfBlocks from './IfBlocks.svelte';
  import ElseBlock from './ElseBlock.svelte';
  let name = "World";
  let src = "/tutorial/image.gif";
  let string = 'this string contains <i>HTML tag</i>'
  let count = 0;
  let numbers = [1, 2, 3, 4];

  $: doubled = count * 2;

  $: console.log('the count is ' + count);

  $: if (count >= 10) {
	alert('count is higth!');
	count = 9;
  }

  $: sum = numbers.reduce((t, n) => t + n, 0);

  function incCount(){
	count += 1;
  }

  function addNum1(){
	numbers.push(numbers.length + 1);
	numbers = numbers;
  }

  function addNum2(){
	numbers = [...numbers, numbers.length + 1];
  }

  const pkg = {
	name: 'svelte', 
	version: 6,
	speed: 'blazing',
	website: 'https://svelte.dev'
  }

</script>

<style>
	p {
		color: purple;
		font-family: 'Comic Sans MS', cursive;
		font-size: 1em;
	}

	.num-style {
		color: blue;
		font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
		font-size: small;
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

<p class="num-style">{numbers.join(' + ')} = {sum}</p>

<button on:click={addNum1}>Add a number</button>

<Nested1 answer = {52}/>
<Nested1 />

<Information name={pkg.name} version={pkg.version} speed={pkg.speed} website={pkg.website} />
<Information {...pkg} />

<IfBlocks />

<ElseBlock />