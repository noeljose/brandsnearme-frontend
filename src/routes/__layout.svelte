<script>
  import Nav from "../components/Nav.svelte";
  import NavTop from "../components/NavTop.svelte";
</script>

<div class="nav">
  <NavTop />
  <Nav />
</div>

<slot />

<style>
  :global(body) {
    min-width: 1300px;
    background-color: rgb(255, 255, 255);
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

  :global(main) {
    width: 80%;
    margin: auto;
  }
</style>
