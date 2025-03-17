
<!-- 

    Name: Ronald Kiefer
    Date: March 17, 2025 Monday
    File: Groups.svelte
    Description: comoponent for binding groups in Svelte.js


-->

<script>

    let scoops = $state(1);
	let flavours = $state(['mint choc chip']);

</script>


<h2 class="title-size">Size</h2>

{#each [1, 2, 3] as number}
	<label class="label">
		<input
			type="radio"
			name="scoops"
			value={number}
			bind:group={scoops}
			class="radio"
		/>

		{number} {number === 1 ? 'scoop' : 'scoops'}
	</label>
{/each}


<h2 class="title-flavours">Flavours<span class="format-span">&nbsp;&nbsp;&nbsp;Default to Mint</span></h2>

{#each ['cookies and cream', 'mint choc chip', 'raspberry ripple'] as flavour}
	<label class="label-flavours">
		<input
			type="checkbox"
			name="flavours"
			value={flavour}
			bind:group={flavours}
		/>

		{flavour}
	</label>
{/each}

{#if flavours.length === 0}
	<p class="p-flavour-select">Please select at least one flavour</p>
{:else if flavours.length > scoops}
	<p class="p-error">Can't order more flavours than scoops!</p>
	<!--  if mint  -->
{:else if flavours[1] === 'mint choc chip' || flavours[0] === 'mint choc chip' || flavours[2] === 'mint choc chip'}
	<p class="p-order-true">
		You ordered {scoops} {scoops === 1 ? 'scoop' : 'scoops'}
		of {flavours}
	</p>
{:else}
	<p class="p-order-false">
		You ordered {scoops} {scoops === 1 ? 'scoop' : 'scoops'}
		of {flavours}
	</p>
{/if}

<div class="format-div">

<!--  first scoop  -->
<div class="format-titles">First</div>
{flavours[0]}


<!--  second scoop  -->
<div class="format-titles">Second</div>
{#if flavours[1]}
	{flavours[1]}
{:else}
	No second flavour
{/if}

<!--  third scoop  -->
<div class="format-titles">Third</div>
{#if flavours[2]}
	{flavours[2]}
{:else}
	No third flavour
{/if}

</div>


<!--   css  -->

<style>


     /*   format title    */
    .title-size {
             text-align: center;
			 background-color: #36454F;
	}


	

	.radio {
		margin-left: 10em;
		color: red;
	}


.label {
		
		color: #D05353;
	}



.title-flavours {
		text-align: center;
		background-color: #36454F;
		color: #D05353;

}

.label-flavours {
		color: #D05353;
		margin-left: 5em;
}


.p-flavour-select {
		color: yellow;
		text-align: center;
		background-color: #36454F;
}

.p-error {
		color: red;
		text-align: center;
		background-color: #36454F;
}




.p-order-true {
		color: green;
		text-align: center;
		background-color: #36454F;
}


.p-order-false {
		color: violet;
		text-align: center;
		background-color: #36454F;
}


.format-titles {
		color: #D05353;
		
		
}

.format-div {
		background-color: #36454F;
		
		text-align: center;
		margin-top: 2em;
		margin-left: 20%;
		margin-right: 20%;
		padding: 1em;
		border-radius: 1em;
}
 
.format-span {
	font-size: 8px;
}

</style>


