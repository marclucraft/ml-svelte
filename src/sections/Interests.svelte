<script>
	import Saos from 'saos';
</script>

<div id="interests">
	<div class="container">
		<Saos
			animation={'fade-in-bottom 1s cubic-bezier(0.35, 0.5, 0.65, 0.95) both'}
		>
			<img class="me" src="images/me.svg" alt="Sketch of me standing" />
		</Saos>
		<div class="text">
			<h3>Personal Interests</h3>
			<ul>
				<li>Skateboarding</li>
				<li>Snowboarding/Skiing</li>
				<li>Golf</li>
				<li>Cooking</li>
				<li>Reading</li>
				<li>
					Learning through Udemy, YouTube, personal projects and exploring open
					source.
				</li>
				<li>Watching whole Netflix series’ in one sitting!</li>
			</ul>
		</div>
	</div>
</div>

<style>
	#interests {
		background-color: #f0f4fe;
		margin-top: -80px;
	}
	#interests::before {
		content: url('../images/separator.svg');
		margin: -4px;
	}
	#interests::after {
		content: url('../images/separator-flipped.svg');
	}

	.container {
		display: flex;
		justify-content: space-evenly;
	}
	.me {
		width: 180px;
		margin: -200px 0 -100px -100px;
		z-index: 169;
	}
	.text {
		width: 500px;
		align-self: center;
		justify-self: center;
	}
	h3 {
		font-size: 1.25em;
		margin-bottom: 10px;
	}
	ul {
		margin-left: 1em;
		column-count: 2;
	}
	li::before {
		content: '\2022';
		color: #3269f9;
		font-weight: bold;
		display: inline-block;
		width: 1em;
		margin-left: -1em;
	}
</style>
