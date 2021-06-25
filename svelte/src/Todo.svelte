<script>
  let todoCount = 0

  function handleClick() {
    todoCount++
  }

  $: doubled = todoCount * 2
</script>

<div>
  <div>count: {todoCount}</div>
  <div>doubled: {doubled}</div>

  <button on:click={handleClick}>Add todo</button>
</div>
