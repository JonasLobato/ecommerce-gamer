<script>
	import { Menu } from 'lucide-svelte';

    let { size="99", absoluteStrokeWidth="true", strokeWidth="2"} = $props()
</script>

<Menu  size={size} absoluteStrokeWidth={absoluteStrokeWidth} strokeWidth={strokeWidth}/>
