<svelte:head>
	<script src="https://cdn.tailwindcss.com"></script>
</svelte:head>

<script>
  import Counter from './lib/Counter.svelte'
  
  let currentFirstMultiple = 1
  let secondMultiple = 1

  const howManyMultiples = 13

  while(currentFirstMultiple<=howManyMultiples && secondMultiple<=howManyMultiples)
  {



    console.log(`${currentFirstMultiple} * ${secondMultiple} = ${currentFirstMultiple*secondMultiple}`)
    secondMultiple++

    if(secondMultiple>12){
      currentFirstMultiple++
      secondMultiple = 1
    }

    if(secondMultiple==1 && currentFirstMultiple<=howManyMultiples){
      console.log(`${currentFirstMultiple} times table`)
    }
    
  }

  </script>

<main>
  <div>
    
  </div>
</main>

<style>

</style>
