<script>
	import Button from './Button.svelte';
</script>

<div>
	<img class="image" src="./images/illustration-hero.svg" alt="" />
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
	h1 {
		font-weight: 500;
		letter-spacing: 0.09px;
		text-align: center;
		color: #242a45;
		line-height: 40px;
	}

	p {
		text-align: center;
	}

	.btn-container {
		display: flex;
		justify-content: space-between;
		padding-top: 2rem;
	}

	.btn-container button {
		padding: 10px 17px;
		font-family: 'Rubik', sans-serif;
		border-radius: 5px;
		border: none;
	}

	.btn-blue {
		background-color: #5267df;
		color: #ffffff;
	}

	.btn-grey {
		background-color: #f7f7f7;
		color: #242a45;
	}
</style>
