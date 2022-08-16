<script>
	 let name="Svelte";
	 let color = "enter any color";
	 const clickHandler=(e)=>{
        color="e.target.value",name="react"
	 }
	 const prevHandle=()=>{
		name="Svelte"
	 }
	 
</script>

<main>
	<h1 style="color:{color}">Hello {name}!</h1>
	<button on:click={clickHandler} on:blur={prevHandle}>Click to change name</button>

	<input type="text" bind:value={color}>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>