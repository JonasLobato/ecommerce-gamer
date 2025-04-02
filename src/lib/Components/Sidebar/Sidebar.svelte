<script>
    import { SquareX } from 'lucide-svelte';

    let {visibleMenu, toggle, ... menuItens} = $props()
    
    console.log(visibleMenu)
</script>
<div
	class="absolute top-0 left-0 h-screen w-2/3 bg-white p-5 xl:hidden"
	class:hidden={!visibleMenu}
>
	<div class="flex justify-end">
		<button onclick={toggle}>
			<SquareX />
		</button>
	</div>
	<ul class="flex flex-col gap-3">
		{#each menuItens as { name, url }}
			<li>
				<a href={url} class=" text-xl">{name}</a>
			</li>
		{/each}
	</ul>
</div>
