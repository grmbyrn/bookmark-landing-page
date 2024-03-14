<script lang="ts">
	import Button from './Button.svelte';

	let buttonText: string = 'Bookmark in one click';
	let paragraphText: string =
		'Organize your bookmarks however you like. Our simple drag-and-drop interface gives you complete control over how you manage your favourite sites.';
	let src: string = 'illustration-features-tab-1';

	function handleClick(text: string) {
		switch (text) {
			case 'Simple Bookmarking':
				buttonText = 'Bookmark in one click';
				paragraphText =
					'Organize your bookmarks however you like. Our simple drag-and-drop interface gives you complete control over how you manage your favourite sites.';
				src = 'illustration-features-tab-1';
				break;
			case 'Speedy Searching':
				buttonText = 'Intelligent search';
				paragraphText =
					'Our powerful search feature will help you find saved sites in no time at all. No need to trawl through all of your bookmarks.';
				src = 'illustration-features-tab-2';
				break;
			case 'Easy Sharing':
				buttonText = 'Share your bookmarks';
				paragraphText =
					'Easily share your bookmarks and collections with others. Create a shareable link that you can send at the click of a button.';
				src = 'illustration-features-tab-3';
				break;
			default:
				break;
		}
	}
</script>

<div class="container">
	<div>
		<h2 class="features-heading">Features</h2>
		<p>
			Our aim is to make it quick and easy for you to access your favourite websites. Your bookmarks
			sync between your devices so you can access them on the go.
		</p>
	</div>
	<div class="btn-container">
		{#each ['Simple Bookmarking', 'Speedy Searching', 'Easy Sharing'] as text}
			<button on:click={() => handleClick(text)}>{text}</button>
		{/each}
	</div>
	<div>
		<div>
			<img src="./images/{src}.svg" alt="" />
		</div>
		<div class="features-container">
			<h2>{buttonText}</h2>
			<p>
				{paragraphText}
			</p>
		</div>
		<Button btn={'More Info'} />
	</div>
</div>

<style>
	.container {
		text-align: center;
		padding-top: 8.75rem;
	}

	.features-heading {
		font-size: 1.5rem;
		letter-spacing: -0.08px;
		color: #242a45;
	}

	.btn-container {
		display: flex;
		flex-direction: column;
		padding-top: 2.5rem;
	}

	.btn-container button {
		border: none;
		background-color: transparent;
		font-family: 'Rubik', sans-serif;
	}

	.btn-container button:hover {
		text-decoration: underline;
		cursor: pointer;
	}

	img {
		padding-top: 4.5rem;
	}

	.features-container {
		padding-top: 2rem;
	}
</style>
