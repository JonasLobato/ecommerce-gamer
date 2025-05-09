<script>
	import Collection from '$lib/Components/Collection/Collection.svelte';
	import Header from '$lib/Sections/Header/Header.svelte';
	import playstation from '$lib/db/product';

</script>

<Header />
<div class="text-white">
	<img src="{playstation.image.src}{playstation.image.name}.jpg" alt="{playstation.image.alt}">
	<h2>{playstation.title}</h2>
	<div>
		<p class="line-through opacity-70">{playstation.price.current.toLocaleString("pt-BR", {style:"currency", currency: "BRL" })}</p>
		<p class="text-green-400">{playstation.price.promotional.toLocaleString("pt-BR", {style:"currency", currency: "BRL" })}</p>
		<p>ou {playstation.price.installments + "x"} de {(playstation.price.promotional / playstation.price.installments).toLocaleString("pt-BR", {style:"currency", currency: "BRL" })}</p>
	</div>
	<p>{playstation.description}</p>
</div>
<Collection collectionName="Consoles"/>