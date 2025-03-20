


<script>
	let flipped = $state(false);
	let symbol = $state('🐦‍🔥');

	function flipCard() {
		flipped = !flipped;
		symbol = flipped ? '🔥' : '🐦‍🔥';
	}

</script>



<nav class="mobile">
	<a href="/events">main</a>
	<a href="/events/#music">music</a>
    <a href="/binding">binding</a>
    <a href="/classesStyles">classes-styles</a>
</nav>



<div class="container-2">
   <div>Name: Ronald Kiefer</div>
   <div>Date: March 20, 2025</div>
   <div>Class: Svelte 5</div>

</div>
<div class="container">
	Flip the card
	<button
		class="card {flipped ? 'flipped' : ''}"
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
  nav {
            background-color: #476C9B;
            padding: 10px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        nav a {
            color: #fff;
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 4px;
            transition: background-color 0.3s;
        }

	.container {
		margin-left: 20px;
	}

	.card {
		width: 10%;
		height: 15%;
		background-color: azure;
		border-radius: 10px;
		margin-top: 20px;
		margin-left: 20px;
	}


	.card.flipped {
		background-color: #DBB4AD;
	}

	.container-2 {
		background-color: #f0f0f0;
		padding: 20px;
		border-radius: 10px;
		box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
		margin-top: 20px;
		text-align: left;
		width: 50%;
	}


</style>






