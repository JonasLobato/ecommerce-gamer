<script>
	import { AlignJustify, SquareX } from 'lucide-svelte';
	import Category from './Category.svelte';
	import Cart from './Cart.svelte';

	let { type = '', visibleMenu, toggle, ...menuItens } = $props();

</script>

<div
	class="absolute top-0 h-screen w-2/3 bg-white p-5 xl:w-96"
	class:hidden={!visibleMenu}
	class:xl:hidden={type=='category'}
	class:left-0={type=='category'}
	class:right-0={type=='cart'}
>
	<div class="flex"
	class:justify-end={type=='category'}
	class:justify-start={type=='cart'}
	>
		<button onclick={toggle}>
			<SquareX />
		</button>
	</div>
	{#if type == 'category'}
		<Category {...menuItens} />
	{:else if type == 'cart'}
		<Cart />
	{/if}
</div>
