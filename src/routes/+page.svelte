<script lang="ts">
	import Email from '$lib/components/Email.svelte';
	import Extension from '$lib/components/Extension.svelte';
	import FAQ from '$lib/components/FAQ.svelte';
	import Features from '$lib/components/Features.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import Header from '$lib/components/Header.svelte';
	import Hero from '$lib/components/Hero.svelte';
</script>

<div class="container">
	<Header />
	<Hero />
	<Features />
	<Extension />
	<FAQ />
</div>
<Email />
<Footer />

<style>
	.container {
		width: 23.438rem;
		background-color: #ffffff;
		display: block;
		margin-left: auto;
		margin-right: auto;
	}
</style>
