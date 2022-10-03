<svelte:head>
	<script src="https://cdn.tailwindcss.com"></script>
</svelte:head>

<script>
  import Counter from './lib/Counter.svelte'
  
  let currentFirstMultiple = 1
  let secondMultiple = 1
  while(currentFirstMultiple<=13 && secondMultiple<=13)
  {

    if(secondMultiple>12){
      currentFirstMultiple++
      secondMultiple = 1
    }

    console.log(`${currentFirstMultiple} * ${secondMultiple} = ${currentFirstMultiple*secondMultiple}`)
    secondMultiple++
    
  }

  </script>

<main>
  <div>
    
  </div>
</main>

<style>

</style>
