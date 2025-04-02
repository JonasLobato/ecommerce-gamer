<script>
	import { Menu, ShoppingCart } from 'lucide-svelte';
	import IconLogo from '../Icons/IconLogo.svelte';
	import Sidebar from '../Sidebar/Sidebar.svelte';

	const menuItens = [
		{name: 'PC', url: '/'},
		{name: 'Playstation', url: '/'},
		{name: 'Xbox', url: '/'},
		{name: 'Nintendo', url: '/'}
	];
	let visibleMenu = false;
	let visibleCart = false;
	function toggle() {
		visibleMenu = !visibleMenu;
	}
	

	
</script>

<nav class="relative bg-pink-50">
	<div class="container flex items-center justify-between py-3">
		<a href="/" class="xl:hidden" onclick={toggle}><Menu /></a>
		<a href="/"><IconLogo customClass="w-32 h-auto" /></a>
		<a href="/"><ShoppingCart /></a>
	</div>
	<Sidebar {...menuItens} {visibleMenu} {toggle}/>
</nav>
