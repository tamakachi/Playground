<svelte:head>
	<script src="https://cdn.tailwindcss.com"></script>
</svelte:head>

  <script>

    let name = 'Kent'

    import Component from "./lib/Component.svelte"
  </script>

<main>
  <h1>My first Svelte component</h1>

  <p>Hello World</p>
  <div> 
    <a href="https://www.youtube.com">Link to my Youtube channel</a>
  </div>

  <Component />
</main>

<style>

  h1{ 
    color: rebeccapurple;
  }
  p{ 
    font-size: 4rem;
    }

</style>
