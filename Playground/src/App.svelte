<svelte:head>
	<script src="https://cdn.tailwindcss.com"></script>
</svelte:head>
<!-- Currently leanring component lifecycle-->
<script>
	import Component from "./lib/Component.svelte"
	
	let element
	let componentReference

	function resetEventHandler(){
		console.log(element.style)
		componentReference.sayHello()
	}
</script>

<!-- bind:this can be used to get a reference to an element for direct manipulation, this is a one way binding-->

<input bind:this={element} />

<hr />

<button on:click={resetEventHandler}>Reset</button>

<Component age='30' bind:this={componentReference}/>
