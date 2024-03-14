<script lang="ts">
	export let isMenuOpen: boolean;
	export let toggleMenu: () => void;
</script>

<div>
	<button on:click={toggleMenu} class:open={isMenuOpen} class="burger">
		{#if !isMenuOpen}
			<img src="./images/icon-hamburger.svg" alt="hamburger" />
		{:else}
			<img src="./images/icon-close.svg" alt="hamburger" />
		{/if}
	</button>
	<nav class:open={isMenuOpen}>
		<slot />
	</nav>
</div>

<style>
	nav {
		display: none;
	}

	nav.open {
		display: block;
	}

	.burger {
		border: none;
		background-color: transparent;
		cursor: pointer;
	}

	@media only screen and (min-width: 1200px) {
		nav {
			display: block;
			position: relative;
		}

		.burger {
			display: none;
		}
	}
</style>
