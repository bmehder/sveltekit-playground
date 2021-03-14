<script>
  export let error;
  export let status;
</script>

<section>
  <p>💩</p>
  <h1>{status}</h1>
  <h3>{error}</h3>
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
  }
  p {
    margin: 0;
    font-size: 12em;
  }
</style>
