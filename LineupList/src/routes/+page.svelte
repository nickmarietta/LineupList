<script lang="ts">
  import { on } from "svelte/events";

  let count = 0;
</script>

<h1 class="title">
  Counter: {count}
</h1>
<div class="button-container">
  <button class="btn" on:click={() => (count += 1)}>Increment</button>
  <button class="btn" on:click={() => (count -= 1)}>Decrement</button>
  <button class="btn" on:click={() => (count *= 3)}>Multiply by 3</button>
  <button class="btn" on:click={() => (count = 0)}>Reset</button>
</div>

<style lang="postcss">
  :global(html) {
    background-color: lightgrey;
  }

  .title {
    font-size: 2.5rem; /* Larger font size */
    font-weight: bold;
    text-align: center;
    margin-bottom: 20px; /* Space below the title */
    color: #1f2937; /* Darker text color */
  }

  .button-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
  }

  .btn {
    background-color: #3b82f6; /* Replace with actual blue color */
    color: white;
    font-weight: bold;
    padding: 1rem 2rem; /* Increase padding */
    margin: 10px; /* Add margin between buttons */
    border-radius: 10px; /* Slightly rounded corners */
    font-size: 1.25rem; /* Increase font size */
    width: 200px; /* Set a consistent width for buttons */
    cursor: pointer; /* Change cursor to pointer on hover */
  }

  .btn:hover {
    background-color: #2563eb; /* Replace with hover blue color */
  }
</style>
