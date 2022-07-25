<script>
	export let text;
	export let url;
	export let target = '_blank';
	export let noopener = false;
</script>

{#if noopener}
	<a href={url} {target} rel="noopener">{text}</a>
{:else}
	<a href={url} {target}>{text}</a>
{/if}

<style>
	a {
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
</style>
