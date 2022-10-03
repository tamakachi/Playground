<svelte:head>
	<script src="https://cdn.tailwindcss.com"></script>
</svelte:head>

<script>
  import Counter from './lib/Counter.svelte'
  const numbers = [0,1,2,3,4,5,6,7,8,9,10]
  const filteredNumbers = numbers.filter((number)=>{
    if (number !== 0){  
    return number % 2 === 0 
    }
  })
  console.log(filteredNumbers)
  </script>

<main>
  <div>
    
  </div>
</main>

<style>

</style>
