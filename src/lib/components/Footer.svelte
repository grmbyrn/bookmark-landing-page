<footer>
	<div>
		<img src="./images/logo-bookmark.svg" class="logo" alt="bookmark logo" />
		<ul class="footer-items">
			<li>Features</li>
			<li>Pricing</li>
			<li>Contact</li>
		</ul>
	</div>
	<div>
		<ul class="social-media">
			<li>
				<img src="./images/icon-facebook.svg" alt="" />
			</li>
			<li>
				<img src="./images/icon-twitter.svg" alt="" />
			</li>
		</ul>
	</div>
</footer>

<style>
	footer {
		background-color: #242a45;
		color: #ffffff;
		padding: 2.5rem;
	}

	.logo {
		margin: 0 auto;
		fill: #ffffff;
	}

	.footer-items,
	.social-media {
		margin-left: 0;
		padding-left: 0;
		list-style: none;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.footer-items {
		flex-direction: column;
		padding-top: 40px;
		gap: 2.5rem;
	}

	.footer-items li {
		font-family: 'Rubik', sans-serif;
		letter-spacing: 1.73px;
		text-transform: uppercase;
	}

	.social-media {
		flex-direction: row;
		gap: 2.5rem;
		padding-top: 3rem;
	}
</style>
