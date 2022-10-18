<svelte:head>
	<script src="https://cdn.tailwindcss.com"></script>
</svelte:head>

  <script>

    let count =1

    // Reactive declaration 
    // Updates the variable whenever the dependency changes (everything right of equals)

    $: double = count * 2
    $: console.log(count)
    $: console.log('reliable double: ', double)

    //Reactive statements
    // Fires the function every time the dependencies change values

    $: add(count,double)

    function add(count,double){
      console.log("Added = ", count + double)
    }

    function increment(){
      count++

    }

    function decrement(){
      count--
    }

    function doSomething(){
      console.log(double)
    }

    </script>

<main>
  <div class="text-center pt-10 font-bold">
    <button 
      class="border border-solid border-black px-[1em] py-[0.6em] rounded-full hover:bg-slate-900 hover:text-white" 
      on:click={decrement}>-
    </button>
    {count} * 2 = {double}
    <button 
      class="border border-solid border-black px-[1em] py-[0.6em] rounded-full hover:bg-slate-900 hover:text-white" 
      on:click={increment}>+
    </button>
    <button 
    class="border border-solid border-black px-[1em] py-[0.6em] rounded-full hover:bg-slate-900 hover:text-white" 
    on:click={doSomething}>Log
  </button>
  </div>
</main>

<style>


</style>
