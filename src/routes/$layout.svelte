<script>
  import Nav from '$components/Nav.svelte';
  import Footer from '$components/Footer.svelte';
</script>

<div>
  <Nav />
  <main>
    <slot />
  </main>
  <Footer />
</div>

<style>
  :global(body) {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    font-family: Arial, Helvetica, sans-serif;
  }
  div {
    display: grid;
    grid-template-rows: auto 1fr auto;
    min-height: 100vh;
  }
  main {
    width: 480px;
    margin: 0 auto;
    padding: 1em;
    text-align: center;
  }
</style>
