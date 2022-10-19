<svelte:head>
	<script src="https://cdn.tailwindcss.com"></script>
</svelte:head>

<script>
 let people = ['Kent','Ben','Max','Ashleigh']
 let count = 0
 $:double = count * 2
 $: console.log(`${count} is ${double} / 2`)
</script>

<main>
  <button on:click={()=>{count--}}>-</button>
  {count} * 2 = {double} 
  <button on:click={()=>{count++ ,console.log(double)}}>+</button>
  <button on:click={()=>{count=0}}>Reset</button>
  <form action="">
    <button on:click|preventDefault={()=>{people.push('Legend'), people = people}}>Push into Array</button>
  </form>
  <p>{people}</p>
</main>

<style>


</style>
