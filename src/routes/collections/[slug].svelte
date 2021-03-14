<script context="module">
  export async function load(ctx) {
    let id = ctx.page.params.slug;
    let post = ctx
      .fetch(`https://jsonplaceholder.typicode.com/posts/${id}`)
      .then((response) => response.json())
      .then((json) => json)
      .catch((err) => console.log(err));
    return {
      props: {
        post,
        id,
      },
    };
  }
</script>

<script>
  export let post;
  export let id;
</script>

{#await post then { title, body }}
  <h1>{title} <small>({id})</small></h1>
  <p>{body}</p>
{/await}

<style>
  h1,
  p {
    text-align: left;
  }
</style>
