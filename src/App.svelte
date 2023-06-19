<!-- App.svelte -->

<script></script>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap");
  :global(body) {
    background-color: var(--background-color);
    height: 100vh;
    margin: 0;
    display: flex; /* Use flexbox for centering */
    align-items: center;
    justify-content: center;
  }

  *{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:"Poppins", sans-serif;
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

    color: #0000;
    padding-bottom: var(--s);
    background: 
      linear-gradient(90deg,
      #94e2d5 10%,
      #89dceb 20%,
      #74c7ec 30%, 
      #89b4fa 40%,
      #b4befe 50%,
      #1e1e2e 0) calc(100% - var(--_p,0%))/200% 100%,
      linear-gradient(
      #89dceb 0
      0) 0% 100%/var(--_p,0%) var(--s) no-repeat;
    -webkit-background-clip: text,padding-box;
    background-clip: text,padding-box;
    transition: 0.5s;
    font-family: "Poppins", sans-serif;
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
