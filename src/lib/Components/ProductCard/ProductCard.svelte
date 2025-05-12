<script>
    import merchandise from "$lib/db/product";
</script>
<div class=" w-auto flex-col bg-gray-200">
    <div>
        <img src="{merchandise.playstation.image.src}{merchandise.playstation.image.name}.jpg" alt="{merchandise.playstation.image.alt}">
    </div>
    <div class="p-2">
        <h2>{merchandise.playstation.title}</h2>
        <div>
		    <p class="line-through opacity-70">{merchandise.playstation.price.current.toLocaleString("pt-BR", {style:"currency", currency: "BRL" })}</p>
		    <p class="text-green-400">{merchandise.playstation.price.promotional.toLocaleString("pt-BR", {style:"currency", currency: "BRL" })}</p>
		    <p>ou {merchandise.playstation.price.installments + "x"} de {(merchandise.playstation.price.promotional / merchandise.playstation.price.installments).toLocaleString("pt-BR", {style:"currency", currency: "BRL" })}</p>
	    </div>
	    <p>{merchandise.playstation.description}</p>
        <button>Adicionar carrinho</button>
    </div>

</div>