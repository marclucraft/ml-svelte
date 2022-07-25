<script>
	import Saos from 'saos';
	import Button from '../components/Button.svelte';
</script>

<div class="container" id="overview">
	<h2>A quick overview of me...</h2>
	<div class="row">
		<div class="col">
			<Saos
				animation={'fade-in-bottom 1s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}
			>
				<img
					class="code icon"
					src="/images/code.svg"
					alt="Markup code icon on blue"
				/>
			</Saos>
			<h3>Current Position</h3>
			<p>
				<strong
					>Digital Developer / Designer for Ford of Britain and Ireland @ TMW
					Unlimited</strong
				> Designing and developing assets for print and digital, followingbrand guidelines.
			</p>
		</div>
		<div class="col">
			<Saos
				animation={'fade-in-bottom 1s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}
			>
				<img
					class="graph icon"
					src="/images/graph.svg"
					alt="Graph icon on blue"
				/>
			</Saos>
			<h3>Key Skills</h3>
			<p>
				Design, Development. Adobe Creative Suite, Affinity Suite, Sketch,
				Visual Studio Code, Mac/PC. JavaScript(ES6/ES7), TypeScript, HTML5,
				CSS3, SASS, Git, NPM, Babel, Webpack, React, Gatsby, Svelte
			</p>
		</div>
		<div class="col">
			<Saos
				animation={'fade-in-bottom 1s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}
			>
				<img
					class="lightbulb icon"
					src="/images/lightbulb.svg"
					alt="Lightbulb icon on blue"
				/>
			</Saos>
			<h3>Learning</h3>
			<p>
				TypeScript: The Complete Developer’s Guide<br />The Complete React
				Developer Course<br />The Modern JavaScript Bootcamp
			</p>
		</div>
	</div>
	<Button
		text="View more on linkedin"
		url="https://www.linkedin.com/in/marclucraft/"
		noopener="true"
	/>
</div>

<style>
	.container {
		padding: 80px 0;
		text-align: center;
	}
	.row {
		display: flex;
		justify-content: space-between;
		margin-bottom: 60px;
	}
	h2 {
		font-size: 2em;
		text-align: center;
		margin-bottom: 69px;
	}
	.col {
		text-align: center;
		width: 30%;
	}
	.icon {
		width: 150px;
	}
	.lightbulb {
		margin-top: -47px;
	}
	h3 {
		font-size: 1.25em;
		margin: 10px 0;
	}
</style>
