


<script>
	

	let value = $state(``);


</script>

<div class="container">
<div>input</div>
<textarea bind:value={value} class="marginTextA"></textarea>
<div>output</div>
<div class="marginOutput">{value}</div>
</div>
<br><br><br><br><br><br>


<style>

.container {
	display: flex;
	flex-direction: column;
	align-items: left;
	justify-content: center;
	margin-top: 2em;
	margin-left: 10%;
	margin-right: 10%;
	background-color: #9DE7F4;
	padding: 1em;
	border-radius: 1em;
	padding-left: 50px;
	padding-right: 30px;
}

.marginTextA {
	margin: 10px;
}

.marginOutput {
	margin: 10px;
	
}

</style>