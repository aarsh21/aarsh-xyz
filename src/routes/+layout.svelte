<script lang="ts">
	import Footer from '$lib/components/Footer.svelte';
	import { Name, profilePicture } from '$lib/profileDetails';
	import { setupViewTransition } from 'sveltekit-view-transition';
	import '../app.css';

	setupViewTransition();
</script>

<svelte:head>
	<title>{Name}</title>
	<link rel="icon" href={profilePicture} />
	<script defer data-domain="aarshpadia.tech" src="https://plausible.io/js/script.js"></script>
</svelte:head>

<div class="relative min-h-screen text-cat_text">
	<slot></slot>

	<Footer />
</div>
