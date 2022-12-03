<script>
    let x = 9;
</script>

{#if x>15}
    <p>{x} is greater than 15</p>
{:else if 7>x}
    <p>{x} is less than 7</p>
{:else}
    <p>{x} is between 7 and 15</p>
{/if}