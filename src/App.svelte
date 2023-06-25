<!-- App.svelte -->

<script></script>

<main>
  <div class="container">
    <h1 class="hover-text">await</h1>
  </div>
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@700&display=swap");

  :root {
    --primary-color: #89dceb;
    --background-color: #1e1e2e;
    --secondary-background-color: #313244;
    --text-color: #cdd6f4;
  }

  :global(body) {
    text-align: center;
    background-color: var(--background-color);
    background: var(--background-color);
    color: var(--text-color);
    font-family: "Poppins", sans-serif;
  }

  :global(.container) {
    margin-top: 22.5rem;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }

  ::selection {
    background-color: var(--primary-color);
    color: var(--background-color);
    border-radius: 5px;
  }

  :global(.hover-text) {
    font-size: 64px;
    transition: font-size 0.3s;
  }

  :global(.hover-text:hover) {
    font-size: 96px;
  }
</style>
