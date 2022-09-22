<script>
  let random = [0]

  const addRandom = () =>{
    
    console.log(random)
    random = [...random, Math.random()]
    // The correct way to push an array into another one, this way refreshes the value bind,
    // When using random.push(Math.random()) the information does not refresh
  }

  let count = 0
  const increment = () => {
    count += 1
  }
</script>

<button on:click={increment}>
  count is {count}
</button>
<button on:click={addRandom}>{random}</button>
