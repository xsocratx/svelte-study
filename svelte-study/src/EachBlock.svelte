<script>
	let cats = [
		{ id: 'J---aiyznGQ', name: 'Keyboard Cat' },
		{ id: 'z_AbfPXTKms', name: 'Maru' },
		{ id: 'OUtn3pvWmpg', name: 'Henri The Existential Cat' },
        { id: 'QH2-TGUlwu4', name: 'Nyan Cat'}
	];
</script>

<h1>The famous cats on YouTube</h1>

<ul>
    {#each cats as cat}
        <li>
            <a target="_blank" href="https://www.youtube.com/watch?v={cat.id}" rel="noreferrer">{cat.name}</a>
        </li>
    {/each}
</ul>