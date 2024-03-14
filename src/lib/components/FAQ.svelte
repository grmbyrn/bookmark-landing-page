<script lang="ts">
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

	function toggleAnswer(id) {
		questions = questions.map((q) => {
			if (q.id === id) {
				return { ...q, isOpen: !q.isOpen };
			} else {
				return { ...q, isOpen: false }; // Close other answers
			}
		});
	}
</script>

<div>
	<h2>Frequently Asked Questions</h2>
	<p>
		Here are some of our FAQs. If you have any other questions you’d like answered please feel free
		to email us.
	</p>

	{#each questions as question}
		<div class="question">
			<div class="question-header" on:click={() => toggleAnswer(question.id)}>
				<h3>{question.question}</h3>
				<button class:open={question.isOpen}>+</button>
			</div>
			{#if question.isOpen}
				<p>{question.answer}</p>
			{/if}
		</div>
	{/each}
</div>

<style>
	.question {
		margin-bottom: 20px;
	}
	h1 {
		font-size: 24px;
		margin-bottom: 10px;
	}
	h3 {
		font-size: 18px;
		margin-bottom: 5px;
	}
	.question-header {
		display: flex;
		align-items: center;
		cursor: pointer;
	}
	.question-header button {
		margin-left: 5px;
		font-size: 16px;
		font-weight: bold;
		transition: transform 0.2s;
	}
	.question-header button.open {
		transform: rotate(45deg);
	}
	p {
		margin-top: 5px;
	}
</style>
