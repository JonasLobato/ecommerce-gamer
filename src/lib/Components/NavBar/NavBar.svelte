<script>
	import { Menu, ShoppingCart } from 'lucide-svelte';
	import IconLogo from '../Icons/IconLogo.svelte';
	import Sidebar from '../Sidebar/Sidebar.svelte';
	import Category from '../Sidebar/Category.svelte';
	import Cart from '../Sidebar/Cart.svelte';

	const menuItens = [
		{name: 'PC', url: '/'},
		{name: 'Playstation', url: '/'},
		{name: 'Xbox', url: '/'},
		{name: 'Nintendo', url: '/'}
	];
	let visibleMenu = $state(false);
	
	function toggle() {
		visibleMenu = !visibleMenu;
	}

	let sidebarType = $state("")
	function toggleSidebarCart() {
		sidebarType = "cart"
		toggle()
	}

	function toggleSidebarCategory() {
		sidebarType = "category"
		toggle()
	}
</script>

<nav class="relative bg-pink-50">
	<div class="container flex items-center justify-between py-3">
		<a href="/" class="lg:hidden" onclick={toggleSidebarCategory}><Menu /></a>
		<a href="/"><IconLogo customClass="w-32 h-auto" /></a>
		<div class="hidden lg:block">
			<ul class="flex flex-row gap-4">
				{#each menuItens as {name, url}}
					<li class=" opacity-70 hover:opacity-100">
						<a href={url} >{name}</a>
					</li>
				{/each}
				
			</ul>
		</div>
		<a href="/" onclick={toggleSidebarCart}><ShoppingCart /></a>
	</div>
	<Sidebar type={sidebarType} {...menuItens} {visibleMenu} {toggle}/>
</nav>
