<script>
    let a = 1;
    let b = 2;
</script>
<style>
    label {
         display: flex 
    }
    input, p { 
        margin: 6px 
    }
</style>

<hr>
<p>Numeric Input</p>

<label>
	<input type=number bind:value={a} min=0 max=10>
	<input type=range bind:value={a} min=0 max=10>
</label>
