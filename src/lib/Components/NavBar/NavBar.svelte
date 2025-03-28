<script>
	import { Menu, ShoppingCart, SquareX } from 'lucide-svelte';
	import IconLogo from '../Icons/IconLogo.svelte';

	const menuItens = [
		{
			name: "PC",
			url: "/"
		},
		{
			name: "Playstation",
			url: "/"
		},
		{
			name: "Xbox",
			url: "/"
		},
		{
			name: "Nintendo",
			url: "/"
		}
	]
</script>

<nav class="relative bg-pink-50">
	<div class="container flex items-center justify-between py-3">
		<a href="/" class="xl:hidden"><Menu /></a>
		<a href="/"><IconLogo customClass="w-32 h-auto" /></a>
		<a href="/"><ShoppingCart /></a>
	</div>
	<div class="absolute top-0 left-0 bg-white h-screen w-2/3 p-5">
		<div>
			<button>
				<SquareX/>
			</button>
		</div>
		<ul class="flex flex-col gap-3">
			{#each menuItens as {name, url}}
			<li>
				<a href="{url}" class=" text-xl">{name}</a>
			</li>
			{/each}
		</ul>
	</div>
</nav>
