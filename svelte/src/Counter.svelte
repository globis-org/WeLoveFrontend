<script lang="ts">
	export let count = 0;
  export let isHello = true
  export let cats = [{
		id: 'default id',
		name: 'default name',
	}]
	export const onDecreaseClick = () => (count -= 1)
  const onIncreaseClick = () => (count += 1)
</script>

<div class="counter">
	<div class="counter-viewport">
		{count}
	</div>

	<button on:click={onDecreaseClick} aria-label="Decrease the counter by one">
		-1
	</button>

	<button on:click={onIncreaseClick} aria-label="Increase the counter by one">
		+1
	</button>
  {#if isHello && count%2 === 0}
    <p>Hello svelte logic</p>
  {/if}

	{#each cats as {id, name}, index}
		<p><span style="font-weight: bold;">{index + 1}.</span> ID:{id} Name:{name}</p>
	{/each}
</div>
