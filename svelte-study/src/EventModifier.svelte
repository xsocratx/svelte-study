<script>
    function handleClick(event){
        alert('clicked')
    }
</script>

<button on:click|once={handleClick}>Click One</button>