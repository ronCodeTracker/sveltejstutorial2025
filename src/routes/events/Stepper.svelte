

<!--
  Name:  Ronald Kiefer
  Date:  3-6-2025  Thursday
  Description:  Sveltekit SV5 - Events 


-->


<script>
    let  { increment, decrement } = $props();

</script>

<button class="buttonNeg" onclick={decrement}>-</button>
<button class="buttonPos" onclick={increment}>+</button>


<style>
	.buttonNeg {
		font-size: 2em;
		padding: 0.5em 1em;
		margin: 0.5em;
		background-color: #00bcd4; /* Light blue color */
        color: #ffffff;
        border: none;
        border-radius: 25px;
        cursor: pointer;
		transition: background-color 0.3s, transform 0.3s, box-shadow 0.3s;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
		margin-left: 40%;
	}

	.buttonPos {

        font-size: 2em;
		padding: 0.5em 1em;
		margin: 0.5em;
		background-color: #00bcd4; /* Light blue color */
		color: #ffffff;
		border: none;
		border-radius: 25px;
		cursor: pointer;
		transition: background-color 0.3s, transform 0.3s, box-shadow 0.3s;
		box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
	}










</style>