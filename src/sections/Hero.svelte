<script>
	import * as animateScroll from 'svelte-scrollto';
	import Saos from 'saos';
</script>

<div class="container hero">
	<div class="text">
		<h1>Hi, I’m Marc...</h1>
		<p>
			Over 14 years of Digital Design, Development, and Project Management
			experience. Expansive knowledge of design software (Adobe CC, Sketch,
			Affinity), and web languages (JavaScript(ES6/ES7), TypeScript, SASS,
			HTML5).
		</p>
		<span on:click={() => animateScroll.scrollTo({ element: '#overview' })}>
			Find out more
		</span>
	</div>
	<Saos
		animation={'fade-in-bottom 1s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}
	>
		<img
			src="/images/me-mac.svg"
			alt="A sketch of me on an unbranded computer"
		/>
	</Saos>
</div>

<style>
	.hero {
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding-top: 60px;
		padding-bottom: 60px;
	}

	.text {
		width: 420px;
	}
	h1 {
		font-size: 3.2rem;
	}
	p {
		margin-bottom: 30px;
	}
	img {
		width: 720px;
		margin-right: -120px;
	}
	span {
		background-color: #3269f9;
		padding: 14px 40px;
		text-transform: uppercase;
		color: #fff;
		border-radius: 32px;
		font-family: 'Overpass', sans-serif;
		font-size: 1rem;
		cursor: pointer;
		text-decoration: none;
		display: inline-block;
	}

	@-webkit-keyframes -global-fade-in-bottom {
		0% {
			-webkit-transform: translateY(50px);
			transform: translateY(50px);
			opacity: 0;
		}
		100% {
			-webkit-transform: translateY(0);
			transform: translateY(0);
			opacity: 1;
		}
	}
	@keyframes -global-fade-in-bottom {
		0% {
			-webkit-transform: translateY(50px);
			transform: translateY(50px);
			opacity: 0;
		}
		100% {
			-webkit-transform: translateY(0);
			transform: translateY(0);
			opacity: 1;
		}
	}
</style>
