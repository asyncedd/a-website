<!-- App.svelte -->

<script></script>

<style>
  :global(body) {
    background-color: var(--background-color);
    height: 100vh;
    margin: 0;
    display: flex; /* Use flexbox for centering */
    align-items: center;
    justify-content: center;
  }

  /* Set the text color to white */
  :global(h1, h2, h3, h4, h5, h6, p, a) {
    color: var(--text-color);
  }

  main {
    text-align: center; /* Center align the content */
  }

  h1 {
    --s: 0.1em;   /* the thickness of the line */
    --c: #89dceb; /* the color */

    color: #0000;
    padding-bottom: var(--s);
    background: 
      linear-gradient(90deg,var(--c) 50%,#1e1e2e 0) calc(100% - var(--_p,0%))/200% 100%;
    -webkit-background-clip: text,padding-box;
    background-clip: text,padding-box;
    transition: 0.5s;
    font-family: system-ui, sans-serif;
    font-size: 5rem;
    cursor: pointer;
  }

  h1:hover {
    --_p: 100%;
    font-size: 6rem; /* Increase the font size when hovered */
  }

  :root {
    --background-color: #11111b;
    --text-color: #cdd6f4;
  }
</style>

<main>
  <h1>Welcome to my Svelte App</h1>
  <p>This is some sample content.</p>
</main>
