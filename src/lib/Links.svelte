<script>
	export let urls = [];
</script>

<ul>
{#each urls as url}
	<li>
		<a href={url[0]}>{url[0]}</a>&nbsp;
		{#if url[1]}
		✔️
		{:else}
		❌
		{/if}
	</li>
{:else}
	<li>
		No links found
	</li>
{/each}
</ul>
