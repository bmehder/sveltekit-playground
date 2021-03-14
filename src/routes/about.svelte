<script>
  import { persist } from '../stores';
  import Counter from '$components/Counter.svelte';
</script>

<h1>About</h1>
<p>The counter component's value is {$persist}.</p>
<main>
  <img src="/1.png" alt="test" />
  <Counter />
</main>

<style>
  main {
    display: grid;
    align-content: center;
  }
  img {
    width: 100%;
  }
</style>
