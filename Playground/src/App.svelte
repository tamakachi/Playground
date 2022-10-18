<svelte:head>
	<script src="https://cdn.tailwindcss.com"></script>
</svelte:head>

  <script>

    
    let imageUrl = 'https://svelte.dev/svelte-logo-horizontal.svg'
  

    let myArray = [0,1]
    let myVariable = 1

    function increment(){
      myArray.push(1)
      myArray = myArray

    }

    function updateVar(){
      myVariable = 2
    }

    import Component from "./lib/Component.svelte"
  </script>

<main>
  <h1>{myArray}</h1>
  <h1>{myVariable}</h1>
  <button on:click={increment}>Push into Array</button>
  <button on:click={updateVar}>Update Var</button>
</main>

<style>

  h1{ 
    color: rebeccapurple;
  }

</style>
