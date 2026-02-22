<script>
  let { children } = $props();
</script>

<div class="weekly-pics-container">
  <h3>Photos of the Week</h3>
  <div class="row">
    {@render children()}
  </div>
</div>

<style>
  .weekly-pics-container {
    margin: 2rem 0;
    margin-bottom: 3rem;
  }

  h3 {
    text-align: center;
    margin-bottom: 1rem;
    color: var(--color-black);
  }

  .row {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
    justify-content: center;
  }

  .row > :global(*) {
    flex: 1;
    min-width: 200px;
    max-width: 300px;
  }
</style>