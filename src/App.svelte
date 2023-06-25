<!-- App.svelte -->
<script>
  import { onMount } from "svelte";

  onMount(() => {
    const link = document.createElement("link");
    link.rel = "stylesheet";
    link.href =
      "https://fonts.googleapis.com/css2?family=Poppins:wght@700&display=swap";
    document.head.appendChild(link);
  });
</script>

<main>
  <div class="container">
    <h1 class="hover-text">await</h1>
  </div>
</main>

<style>
  :root {
    --primary-color: #89dceb;
    --surface0: #313244;
    --background-color: #1e1e2e;
    --secondary-background-color: #313244;
    --text-color: #cdd6f4;
  }

  :global(body) {
    text-align: center;
    background-color: var(--background-color);
    color: var(--text-color);
    font-family: "Poppins", sans-serif;
  }

  .container {
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

  .hover-text {
    font-size: 64px;
    transition: font-size 0.3s, color 0.3s;
  }

  .hover-text:hover {
    font-size: 96px;
    color: var(--surface0);
  }

  h1:before {
    content: "await";
    position: absolute;
    color: var(--primary-color);
    top: 26rem;
    left: 0;
    width: 0%;
    overflow: hidden;
    transition: all 0.5s;
  }

  h1:hover:before {
    width: 103%;
  }
</style>
