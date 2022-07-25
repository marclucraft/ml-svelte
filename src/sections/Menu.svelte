<script>
	import * as animateScroll from 'svelte-scrollto';

	let isChanged = false;

	let links = [
		{
			anchor: '#overview',
			title: 'Overview',
		},
		{
			anchor: '#interests',
			title: 'Interests',
		},
		{
			anchor: '#examples',
			title: 'Examples',
		},
		{
			anchor: '#contact',
			title: 'Contact',
		},
	];

	function handleClick() {
		isChanged = !isChanged;
	}
</script>

<header>
	<div class="container menu">
		<a class="my-name" href="/">Marc Lucraft</a>

		<div class={`burger ${isChanged ? 'change' : ''}`} on:click={handleClick}>
			<div class="bar1" />
			<div class="bar2" />
			<div class="bar3" />
		</div>

		<nav>
			{#each links as { anchor, title }}
				<span on:click={() => animateScroll.scrollTo({ element: anchor })}>
					{title}
				</span>
			{/each}
		</nav>
	</div>
</header>

<style>
	.menu {
		display: flex;
		justify-content: space-between;
		align-items: center;
		font-family: 'Chivo', sans-serif;
		text-transform: uppercase;
		padding-top: 30px;
		padding-bottom: 30px;
	}

	.my-name {
		font-weight: 900;
		text-decoration: none;
		color: #000;
		font-size: 23px;
	}

	nav span {
		text-decoration: none;
		color: #000;
		font-size: 16px;
		margin-left: 15px;
		cursor: pointer;
	}

	.burger {
		display: none;
		cursor: pointer;
	}

	.bar1,
	.bar2,
	.bar3 {
		width: 35px;
		height: 5px;
		background-color: #000;
		margin: 6px 0;
		transition: 0.4s;
	}

	.change .bar1 {
		-webkit-transform: rotate(-45deg) translate(-9px, 6px);
		transform: rotate(-45deg) translate(-9px, 6px);
	}
	.change .bar2 {
		opacity: 0;
	}

	.change .bar3 {
		-webkit-transform: rotate(45deg) translate(-8px, -8px);
		transform: rotate(45deg) translate(-8px, -8px);
	}

	@media (max-width: 700px) {
		.burger {
			display: inline-block;
		}
		nav {
			display: none;
		}
	}
</style>
