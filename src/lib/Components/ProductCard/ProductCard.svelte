<script>
	let { image, title, price, description } = $props();
    const priceInInstallments = (price.promotional / price.installments)
    function formatPrice(value){
        return value.toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' })
    }
    // console.log(image)
</script>

<div class=" w-auto flex-col bg-gray-200">
	<div>
		<img src="{image.src}{image.name}.jpg" alt={image.alt} />
	</div>
	<div class="p-2">
		<h2>{title}</h2>
		<div>
			<p class="line-through opacity-70">
				{formatPrice(price.current)}
			</p>
			<p class="text-green-400">
				{formatPrice(price.promotional)}
			</p>
			<p>
				ou {price.installments + 'x'} de {formatPrice(priceInInstallments)}
			</p>
		</div>
		<p>{description}</p>
		<button>Adicionar carrinho</button>
	</div>
</div>
