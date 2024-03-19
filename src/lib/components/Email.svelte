<script lang="ts">
	let email: string = '';
	let isValidEmail: boolean = true;
	let isButtonClicked = false;

	const validateEmail = () => {
		const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
		isValidEmail = regex.test(email);
	};

	const handleSubmit = () => {
		isButtonClicked = true;
		if (isValidEmail) {
			// Email is valid, proceed with the submission
		} else {
			// Email is not valid, display an error message
			console.log('Invalid email');
		}
	};
</script>

<div class="container">
	<p class="email-msg">35,000+ already joined</p>
	<h4>Stay up-to-date with what we're doing</h4>
	<div class="email">
		<input
			type="email"
			placeholder="Enter your email..."
			bind:value={email}
			on:input={validateEmail}
		/>
		{#if isButtonClicked && !isValidEmail}
			<p class="invalid-email">Whoops, make sure it's an email</p>
		{/if}
		<button on:click={handleSubmit}>Contact Us</button>
	</div>
</div>

<style>
	.container {
		background-color: #5267df;
		margin-top: 7.6875rem;
		text-align: center;
		padding-block: 3.75rem 2.375rem;
		padding-inline: 2rem;
	}

	p,
	h4 {
		color: #ffffff;
	}

	.email-msg {
		letter-spacing: 4.62px;
	}

	h4 {
		font-size: 1.5rem;
		letter-spacing: -0.08px;
		line-height: 2rem;
	}

	.email {
		display: flex;
		flex-direction: column;
		padding-inline: 2rem;
	}

	input {
		padding: 10px 20px;
		font-family: 'Rubik', sans-serif;
		margin-top: 2rem;
	}

	.invalid-email {
		font-style: italic;
	}

	.email button {
		margin-top: 1rem;
		background-color: #fa5959;
		border: none;
		border-radius: 5px;
		padding: 10px;
		font-family: 'Rubik', sans-serif;
		color: #ffffff;
	}
</style>
