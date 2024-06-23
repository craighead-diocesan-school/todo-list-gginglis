<script>
  import Header from "$lib/Header.svelte";
  let tasks = [];

  function addTask() {
    tasks = [...tasks, ""];
  }
</script>

<Header />

<main>
  <button on:click={addTask}>📝 Add</button>

  {#each tasks as task, index}
    <div class="task">
      <input bind:value={tasks[index]} />
    </div>
  {/each}
  <!-- <h2>SvelteKit</h2>

  <p>
    Welcome to coding with SvelteKit, a modern JavaScript framework that makes
    it easy to code great apps.
  </p> -->
</main>

<footer>
  <p>&copy; Craighead Diocesan School 2024</p>
</footer>

<style>
  .task {
    display: block;
  }
</style>
