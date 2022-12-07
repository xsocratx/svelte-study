<script>
    let yes = false;
</script>
<hr>
<label>
    <input type="checkbox" bind:checked={yes}>
    Yes!
</label>

{#if yes}
    <p>Thank you!</p>
{:else}
    <p>No</p>
{/if}

<button disabled={!yes}>Subscribe</button>