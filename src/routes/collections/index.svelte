<script context="module">
  export async function load(ctx) {
    const posts = ctx
      .fetch('https://jsonplaceholder.typicode.com/posts/')
      .then((response) => response.json())
      .then((json) => json)
      .catch((err) => console.log(err));
    return {
      props: {
        posts,
      },
    };
  }
</script>

<script>
  export let posts;
</script>

{#await posts then posts}
  <ul>
    {#each posts as post}
      <li>
        <a sveltekit:prefetch href="/collections/{post.id}">{post.title}</a>
      </li>
    {/each}
  </ul>
{/await}

<style>
  ul {
    text-align: left;
  }
  li {
    line-height: 1.5;
  }
</style>
