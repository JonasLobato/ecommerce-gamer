<script>
	import { Search } from 'lucide-svelte';

    let { size="99",strokeWidth="2"} = $props()
</script>

<Search  size={size} strokeWidth={strokeWidth}/>
