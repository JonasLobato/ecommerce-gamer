<script>
	import { ShoppingCart } from 'lucide-svelte';

    let {strokeWidth="2"} = $props()
</script>
<ShoppingCart strokeWidth={strokeWidth}/>
