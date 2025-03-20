

<script>

let flipped = $state(false);
let symbol = $state('🐴');

	function flipCard() {
		flipped = !flipped;
		symbol = flipped ? '🦄' : '🐴';
	}



</script>






<div class="container">
	Flip the card
	<button
		class="card"
		style:background-color={flipped ? '#DBB4AD' : 'azure'}
		style:border-radius=10px
		onclick={() => {
			//flipped = !flipped;
			//symbol = flipped ? '🔥' : '🐦‍🔥';
		    flipCard();
		}}
	>
		<div>
			<span class="symbol">{symbol}</span>
		</div>
		
	</button>
</div>


<style>

.container {
		margin-left: 20px;
	}

.card {
		width: 10%;
		height: 15%;
		background-color: azure;
		
		margin-top: 20px;
		margin-left: 20px;
	}





</style>

