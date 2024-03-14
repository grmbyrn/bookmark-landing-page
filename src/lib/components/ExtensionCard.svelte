<script lang="ts">
	export let src: string = '';
	export let alt: string = '';
	export let browser: string = '';
	export let version: number;
</script>

<div>
	<img {src} {alt} />
	<h3>Add to {browser}</h3>
	<p>Minimum version {version}</p>
	<button>Add & Install Extension</button>
</div>
