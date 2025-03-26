<script>
	import { Menu } from 'lucide-svelte';

    let {tw="24px", strokeWidth="2"} = $props()
</script>

<Menu width={tw} height={tw} strokeWidth={strokeWidth}/>
