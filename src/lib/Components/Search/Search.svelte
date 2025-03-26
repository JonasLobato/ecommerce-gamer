<script>
	import { Search } from 'lucide-svelte';

    let {strokeWidth="2"} = $props()
</script>

<Search strokeWidth={strokeWidth}/>
