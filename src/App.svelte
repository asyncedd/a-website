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
    transition: font-size 0.3s, color 0.3s, -webkit-text-stroke 0.3s;
  }

  .hover-text:hover {
    font-size: 96px;
    -webkit-text-stroke: 3px var(--surface0);
    color: transparent;
  }

  h1:before {
    content: "await";
    position: absolute;
    -webkit-text-stroke: 0px transparent;
    top: 25rem;
    left: 0;
    width: 100%;
    overflow: hidden;
    transition: all 0.5s;
    color: transparent;
  }

  h1:hover:before {
    color: var(--primary-color);
    width: 103%;
  }

  h1:after {
    content: "await";
    position: absolute;
    color: var(--surface0);
    -webkit-text-stroke: 0px transparent;
    top: 23rem;
    left: 0;
    width: 100%;
    overflow: hidden;
    transition: all 0.5s;
    z-index: -1;
    color: transparent;
  }

  h1:hover:after {
    width: 100%;
    -webkit-text-stroke: 3px var(--surface0);
  }

  h1 {
    -webkit-text-stroke: 0px var(--text-color);
  }
</style>
