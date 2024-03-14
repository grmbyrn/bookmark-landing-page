<script lang="ts">
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

<div>
	<div>
		<h2>Features</h2>
		<p>
			Our aim is to make it quick and easy for you to access your favourite websites. Your bookmarks
			sync between your devices so you can access them on the go.
		</p>
	</div>
	<div>
		{#each ['Simple Bookmarking', 'Speedy Searching', 'Easy Sharing'] as text}
			<button on:click={() => handleClick(text)}>{text}</button>
		{/each}
	</div>
	<div>
		<div>
			<img src="./images/{src}.svg" alt="" />
		</div>
		<div>
			<h2>{buttonText}</h2>
			<p>
				{paragraphText}
			</p>
			<button>More info</button>
		</div>
	</div>
</div>
