<svelte:head>
	<script src="https://cdn.tailwindcss.com"></script>
</svelte:head>

<script>
	let scoops = 1;
	let flavours = ['Mint choc chip'];

	function join(flavours) {
		if (flavours.length === 1) return flavours[0];
		return `${flavours.slice(0, -1).join(', ')} and ${flavours[flavours.length - 1]}`;
	}
</script>

<h2>Size</h2>

<label>
	<input type=radio bind:group={scoops} name="scoops" value={1}>
	One scoop
</label>

<label>
	<input type=radio bind:group={scoops} name="scoops" value={2}>
	Two scoops
</label>

<label>
	<input type=radio bind:group={scoops} name="scoops" value={3}>
	Three scoops
</label>

<p>scoops: {scoops}</p>

<h2>Flavours</h2>

<label>
	<input type=checkbox bind:group={flavours} name="flavours" value="Cookies and cream">
	Cookies and cream
</label>

<label>
	<input type=checkbox bind:group={flavours} name="flavours" value="Mint choc chip">
	Mint choc chip
</label>

<label>
	<input type=checkbox bind:group={flavours} name="flavours" value="Raspberry ripple">
	Raspberry ripple
</label>

<p>{flavours}</p>