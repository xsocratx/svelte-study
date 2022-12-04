<script>
    import {createEventDispatcher} from 'svelte';

    const dispatch = createEventDispatcher();

    function sayHello(){
        dispatch('message', {text: 'hello from dispatch!'});
    }
</script>

<button on:click={sayHello}>Click for hello</button>