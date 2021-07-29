<script lang="ts">
	export let count = 0;
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
</div>
