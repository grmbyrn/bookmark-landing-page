<script lang="ts">
	import Button from './Button.svelte';

	export let src: string = '';
	export let alt: string = '';
	export let browser: string = '';
	export let version: number;
</script>

<div class="container">
	<img {src} {alt} class="logo-img" />
	<h3>Add to {browser}</h3>
	<p>Minimum version {version}</p>
	<img src="./images/bg-dots.svg" alt="dots" class="dots-img" />
	<div class="btn">
		<Button btn={'Add & Install Extension'} />
	</div>
</div>

<style>
	.container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		margin: 0 auto;
		align-items: center;
		border-radius: 15px;
		margin-block: 2.5rem;
		box-shadow:
			rgba(0, 0, 0, 0.1) 0px 20px 25px -5px,
			rgba(0, 0, 0, 0.04) 0px 10px 10px -5px;
		width: 280px;
	}

	.logo-img {
		margin-top: 3.0625rem;
	}

	h3 {
		margin-top: 2rem;
	}

	p {
		margin-top: 6px;
	}

	.dots-img {
		margin-top: 2rem;
	}

	.btn {
		margin-block: 1.5rem;
	}
</style>
