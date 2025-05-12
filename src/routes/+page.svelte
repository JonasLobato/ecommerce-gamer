<script>
	import Collection from '$lib/Components/Collection/Collection.svelte';
	import Header from '$lib/Sections/Header/Header.svelte';
	import {playstation, xbox, nintendo} from '$lib/db/products'

</script>

<Header />
<Collection productCategory={playstation} collectionName="Playstation"/>
<Collection productCategory={xbox} collectionName="Xbox"/>
<Collection productCategory={nintendo} collectionName="Nintendo"/>