<script lang="ts">
  import { on } from "svelte/events";

    let count = 0;
</script>

<h1>Counter: {count}</h1>
<button on:click={() => count += 1}>Increment</button>
<button on:click={() => count -= 1}>Decrement</button>
<button on:click={() => count *= 3}>Multiply by 3</button>
<button on:click={() => count = 0}>Reset</button>