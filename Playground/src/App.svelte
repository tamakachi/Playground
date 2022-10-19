<svelte:head>
	<script src="https://cdn.tailwindcss.com"></script>
</svelte:head>

<script>

  import { tick } from 'svelte'
  import Component from './lib/Component.svelte'

 let people = ['Kent','Ben','Max','Ashleigh']
 let details = {username:'Kent',email:'kent@gmail.com',age:30}
 let count = 0
 $:double = count * 2
 $: console.log(`${count} is ${double} / 2`)

 let greetUser = (event) =>{
    console.log('Greetings ' + event.detail)
 }

</script>

<main>
  <button on:click={()=>{count--}}>-</button>
  {count} * 2 = {double} 
  <button on:click={()=>{count++ ,tick().then(()=>{console.log(double)})}}>+</button>
  <button on:click={()=>{count=0}}>Reset</button>
  <form action="">
    <button on:click|preventDefault={()=>{people.push('Legend'), people = people}}>Push into Array</button>
  </form>
  <p>{people}</p>
  <Component {...details} on:greet={greetUser}></Component>
</main>

<style>


</style>
