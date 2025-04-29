<script>
    let {...menuItens} = $props()
</script>
<ul class="flex flex-col gap-3">
    {#each menuItens as { name, url }}
        <li>
            <a href={url} class=" text-xl">{name}</a>
        </li>
    {/each}
</ul>