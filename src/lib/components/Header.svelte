<script lang="ts">
	import AnimatedHamburger from './AnimatedHamburger.svelte';

	let isMenuOpen = false;

	function toggleMenu() {
		isMenuOpen = !isMenuOpen;
	}
</script>

<header>
	<a href="/">
		<img src="./images/logo-bookmark.svg" alt="" />
	</a>
	<AnimatedHamburger {isMenuOpen} {toggleMenu}>
		<div>
			<ul>
				<li>
					<a href="/">Features</a>
				</li>
				<li>
					<a href="/">Pricing</a>
				</li>
				<li>
					<a href="/">Contact</a>
				</li>
				<li>
					<a href="/">Login</a>
				</li>
			</ul>
		</div>
	</AnimatedHamburger>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		padding: 2.5rem;
	}

	ul {
		margin: 0 auto;
	}

	@media only screen and (min-width: 1200px) {
		ul {
			display: flex;
			padding-left: 0;
			margin-left: 0;
			list-style: none;
		}

		a {
			text-decoration: none;
		}
	}
</style>
