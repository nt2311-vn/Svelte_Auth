<script>
	import { onMount } from 'svelte';
	import { auth } from '../lib/firebase/firebase.client.js';
	onMount(() => {
		const unsubscribe = auth.onAuthStateChanged((user) => {
			console.log(user);
		});
	});
</script>

<slot />
