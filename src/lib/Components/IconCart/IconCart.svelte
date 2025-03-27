<script>
	import { ShoppingCart } from 'lucide-svelte';

    let { size="99",strokeWidth="2" } = $props()
</script>
<ShoppingCart size={size} strokeWidth={strokeWidth}/>
