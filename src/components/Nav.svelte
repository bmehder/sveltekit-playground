<script>
  import { page } from '$app/stores';
</script>

<nav>
  <ul>
    <li><a class:selected={$page.path === '/'} href="/">Home</a></li>
    <li><a class:selected={$page.path === '/about'} href="/about">About</a></li>
    <li>
      <a class:selected={$page.path === '/services'} href="/services"
        >Services</a
      >
    </li>
    <li>
      <a
        class:selected={$page.path === '/collections' ||
          $page.path.includes('/collections')}
        href="/collections">Collections</a
      >
    </li>
    <li>
      <a class:selected={$page.path === '/contact'} href="/contact">Contact</a>
    </li>
  </ul>
</nav>

<style>
  ul {
    display: flex;
    justify-content: center;
    gap: 1em;
    margin: 0;
    padding: 2em 0;
    background: #333;
    color: azure;
  }
  ul {
    list-style: none;
  }
  a {
    font-weight: bold;
    color: azure;
    text-decoration: none;
  }
  .selected {
    padding-bottom: 0.5em;
    border-bottom: 2px solid azure;
  }
</style>
