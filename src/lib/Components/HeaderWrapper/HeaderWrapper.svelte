<script>
	import IconCart from '../IconCart/IconCart.svelte';
	import IconMenu from '../IconMenu/IconMenu.svelte';
	import IconLogo from '../Logoipsum-350/IconLogo.svelte';
	import Search from '../Search/Search.svelte';
</script>

<section class=" bg-gray-600">
	<div class="container py-3 px-5 flex justify-between">
		<div class="flex gap-1">
			<a href="none"><IconMenu tw="42px" strokeWidth="2"/></a>
			<a href="none"><Search strokeWidth="2"/></a>
		</div>
		<a href="none"><IconLogo lw="120px" lh="100%"/></a>
		<a href="none"><IconCart strokeWidth="2"/></a>
	</div>
</section>
