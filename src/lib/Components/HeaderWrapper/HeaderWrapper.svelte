<script>
	import IconCart from '../IconCart/IconCart.svelte';
	import IconMenu from '../IconMenu/IconMenu.svelte';
	import IconLogo from '../Logoipsum-350/IconLogo.svelte';
	import Search from '../Search/Search.svelte';
</script>

<section class=" bg-amber-50">
	<div class="container py-3 px-5 flex justify-between">
		<div class="flex gap-2">
			<a href="none" class=" flex items-center justify-center"><IconMenu size="25" strokeWidth="2"/></a>
			<a href="none" class=" flex items-center justify-center"><Search size="25" strokeWidth="2"/></a>
		</div>
		<a href="none" class=" flex items-center justify-center"><IconLogo lw="120px" lh="100%"/></a>
		<a href="none" class=" flex items-center justify-center"><IconCart size="25" strokeWidth="2"/></a>
	</div>
</section>
