
<script>
	import Nav from '.././Nav.svelte';
    import Thing from './Thing.svelte';
    import { roll } from '../.././utils';


    if (roll) {
		console.log('roll is true');
	} else {
		console.log('roll is false');
	}



	let count = $state(0);

	function increment() {
		count += 1;
	}

    const colors = ['red', 'orange', 'yellow', 'green', 'blue', 'indigo', 'violet'];
	let selected = $state(colors[6]);

    let things = $state([
		{ id: 1, name: 'apple' },
		{ id: 2, name: 'banana' },
		{ id: 3, name: 'carrot' },
		{ id: 4, name: 'doughnut' },
		{ id: 5, name: 'egg' }
	]);

    let promise = $state(roll());


</script>




<Nav />

<p class="headingLogic">
     This part of the tutorial is on logic and particularly if command
</p>

<button onclick={increment}>
	Clicked {count}
	{count === 1 ? 'time' : 'times'}
</button>




{#if count > 10}
	<p class="miracleText">{count} is greater than 10</p>
{:else if count < 10}
	<p class="miracleText">{count} is less than 10</p>
{:else}
	<p class="miracleText">{count} is equal to 10</p>
{/if}



<div class="mainCard displayBlock" >

<h1 style="color: {selected}" class="titleRound">Pick a colour</h1>


<div class="divdiv">
	{#each colors as color, i}
		<button class="btnRound"
			style="background: {color}"
			aria-label={color}
			aria-current={selected === color}
			onclick={() => selected = color}
		>{i + 1}</button>
	{/each}
</div>
</div>

<!--  things section  -->

<button onclick={() => things.shift()}>
	Remove first thing
</button>

{#each things as thing (thing.id)}
	<Thing name={thing.name} />
{/each}

<!-- roll  -->

<button onclick={() => promise = roll()}>
	roll the dice
</button>


{#await promise}
	<p class="htmlDice">...rolling</p>
{:then number}
	<p class="htmlDice">you rolled a {number}!</p>
{:catch error}
	<p style="color: red" class="htmlDice">{error.message}</p>
{/await}




<br><br><br><br><br>

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


        nav a:hover {
            background-color: #0000CC;
        }


        button {
            padding: 10px 20px;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            margin: 10px;
            transition: background-color 0.3s, transform 0.3s;
        }
    button {
            background-color: #42a5f5;
        }
        button:hover {
            background-color: #1e88e5;
            transform: scale(1.05);
        }


        button:active {
            background-color: #1565c0;
            transform: scale(1);
        }
        
       .headingLogic {

         margin-top: 3em;
         margin-bottom: 3em;
         font-family: 'Comic Sans MS', cursive;
         text-align: center;
       }

       .miracleText {
           font-family: 'Comic Sans MS', cursive;
           margin-left: 30%;
       }


       h1 {


		transition: color 0.2s;
		font-size: 2rem;
		font-weight: 700;
	}

    .divdiv {

        display: grid;
		grid-template-columns: repeat(7, 1fr);
		grid-gap: 5px;
		max-width: 400px;
        margin-left: 5em;
    }


    .btnRound {
        aspect-ratio: 1;
		border-radius: 50%;
		background: var(--color, #fff);
		transform: translate(-2px,-2px);
		filter: drop-shadow(2px 2px 3px rgba(0,0,0,0.2));
		transition: all 0.1s;
		color: black;
		font-weight: 700;
		font-size: 2rem;
        


    }


    .btnRound[aria-current="true"] {
		transform: none;
		filter: none;
		box-shadow: inset 3px 3px 4px rgba(0,0,0,0.2);
        
	}

    .titleRound {
        margin-top: 2em;
        margin-bottom: 2em;
        padding-top: 1em;
        padding-left: 1em;
    }

    .mainCard {
            font-family: Arial, sans-serif;
            background-color: azure;
            display: flex;
            justify-content: left;
            align-items: center;
            height: 30vh;
            margin: 0;
            margin-top: 25px;
            
            padding-bottom: 10em;
        }


        .displayBlock {

                display: block;
        }


        .htmlDice {
            font-family: 'Comic Sans MS', cursive;
            margin-left: 30%;
        }


</style>








