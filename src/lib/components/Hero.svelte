<script>
	import Button from './Button.svelte';
</script>

<div class="container">
	<div class="image-container">
		<img class="image" src="./images/illustration-hero.svg" alt="" />
		<div class="rectangle"></div>
	</div>
	<h1>A Simple Bookmark Manager</h1>
	<p>
		A clean and simple interface to organize your favourite websites. Open a new browser tab and see
		your sites load instantly. Try it for free.
	</p>
	<div class="btn-container">
		<Button btn={'Get it on Chrome'} />
		<button class="btn-grey"> Get it on Firefox </button>
	</div>
</div>

<style>
	.container {
		margin-top: 5rem;
	}

	.rectangle {
		width: 20rem;
		margin-top: -12rem;
		margin-left: 10rem;
		background: #5267df;
		height: 12.6875rem;
		border-radius: 31.65rem 0 0 31.65rem;
		z-index: -1;
	}

	h1 {
		font-weight: 500;
		letter-spacing: 0.09px;
		text-align: center;
		color: #242a45;
		line-height: 40px;
	}

	p {
		text-align: center;
		line-height: 25px;
		color: #242a45;
	}

	.btn-container {
		display: flex;
		justify-content: space-between;
		padding-top: 2rem;
	}

	.btn-container button {
		padding: 10px 1.5rem;
		font-family: 'Rubik', sans-serif;
		border-radius: 5px;
		border: none;
	}

	.btn-grey {
		background-color: #f7f7f7;
		color: #242a45;
	}
</style>
