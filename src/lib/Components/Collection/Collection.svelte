<script>
	import ProductCard from '../ProductCard/ProductCard.svelte';

    let {collectionName="Coleção sem nome"} = $props()
</script>

<section class=" space-y-5 py-5">
    <div class="container">
        <h2 class=" text-white text-xl">{collectionName}</h2>
    </div>
	<div class="container grid grid-cols-2 gap-3 md:grid-cols-3 lg:grid-cols-5">
		<ProductCard />
		<ProductCard />
		<ProductCard />
		<ProductCard />
	</div>
</section>
