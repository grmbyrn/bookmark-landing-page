<script lang="ts">
	import ExtensionCard from './ExtensionCard.svelte';

	const extensions = [
		{ src: '/images/logo-chrome.svg', alt: 'Chrome Logo', browser: 'Chrome', version: 62 },
		{ src: '/images/logo-firefox.svg', alt: 'Firefox Logo', browser: 'Firefox', version: 55 },
		{ src: '/images/logo-opera.svg', alt: 'Opera Logo', browser: 'Opera', version: 46 }
	];
</script>

<div class="container">
	<div>
		<h2>Download the extension</h2>
		<p>
			We’ve got more browsers in the pipeline. Please do let us know if you’ve got a favourite you’d
			like us to prioritize.
		</p>
	</div>
	<div class="card-container">
		{#each extensions as extension}
			<ExtensionCard {...extension} />
		{/each}
	</div>
</div>

<style>
	.container {
		margin-top: 4.8125rem;
		text-align: center;
	}
</style>
