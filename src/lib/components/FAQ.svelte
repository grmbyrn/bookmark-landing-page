<script lang="ts">
	import Button from './Button.svelte';

	let questions = [
		{
			id: 1,
			question: 'What is Bookmark?',
			answer:
				'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce tincidunt justo eget ultricies fringilla. Phasellus blandit ipsum quis quam ornare mattis.',
			isOpen: false
		},
		{
			id: 2,
			question: 'How can I request a new browser?',
			answer:
				'Vivamus luctus eros aliquet convallis ultricies. Mauris augue massa, ultricies non ligula. Suspendisse imperdiet. Vivamus luctus eros aliquet convallis ultricies. Mauris augue massa, ultricies non ligula. Suspendisse imperdie tVivamus luctus eros aliquet convallis ultricies. Mauris augue massa, ultricies non ligula. Suspendisse imperdiet.',
			isOpen: false
		},
		{
			id: 3,
			question: 'Is there a mobile app?',
			answer:
				'Sed consectetur quam id neque fermentum accumsan. Praesent luctus vestibulum dolor, ut condimentum urna vulputate eget. Cras in ligula quis est pharetra mattis sit amet pharetra purus. Sed sollicitudin ex et ultricies bibendum.',
			isOpen: false
		},
		{
			id: 4,
			question: 'What about other Chromium browsers?',
			answer:
				'Integer condimentum ipsum id imperdiet finibus. Vivamus in placerat mi, at euismod dui. Aliquam vitae neque eget nisl gravida pellentesque non ut velit.',
			isOpen: false
		}
	];

	function toggleAnswer(id: number) {
		questions = questions.map((q) => {
			if (q.id === id) {
				return { ...q, isOpen: !q.isOpen };
			} else {
				return { ...q, isOpen: false }; // Close other answers
			}
		});
	}
</script>

<div class="container">
	<h2>Frequently Asked Questions</h2>
	<p>
		Here are some of our FAQs. If you have any other questions you’d like answered please feel free
		to email us.
	</p>

	<div class="question-container">
		{#each questions as question}
			<div class="question-content">
				<button class="question-header" on:click={() => toggleAnswer(question.id)}>
					<h3>{question.question}</h3>
					<img class:open={question.isOpen} src="./images/icon-arrow.svg" alt="" />
				</button>
			</div>
			{#if question.isOpen}
				<p class="answer">{question.answer}</p>
			{/if}
		{/each}
	</div>

	<div class="btn-container">
		<Button btn={'More Info'} />
	</div>
</div>

<style>
	.container {
		padding-inline: 2rem;
		text-align: center;
	}

	.question-container {
		margin-top: 4rem;
	}

	.question-content {
		border-bottom: 0.1px solid #979797;
		padding-block: 12px;
	}

	.question-header {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: space-between;
		width: 313px;
		cursor: pointer;
		border: none;
		background-color: transparent;
	}

	h3 {
		font-size: 15px;
		font-weight: 400;
	}

	.question-header img.open {
		transform: rotate(180deg);
	}

	.answer {
		margin-top: 1.5rem;
		line-height: 30px;
		text-align: left;
	}

	.btn-container {
		margin-top: 3rem;
	}
</style>
