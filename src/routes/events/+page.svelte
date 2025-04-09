

<script>

//  Name:  Ronald Kiefer
//  Date:  3-5-2025  Wednesday
//  Description:  Sveltekit SV5 - Events - Pointer Events - Pointer Move
import Nav from './NavTwo.svelte';
import Stepper from './Stepper.svelte';
import BigButton from './BigButton.svelte';
import sound from './sound.mp3';



	let m = $state({ x: 0, y: 0 });

	function onpointermove(event) {
		m.x = event.clientX;
		m.y = event.clientY;
	}

	let value = $state(0);


	const audio = new Audio();
	audio.src = sound;


	function hitit() {
		audio.load();
		audio.play();
	}

	



</script>

<!--

<Nav />

-->

<nav>
	<a href="/events">main</a>
	<a href="#music">music</a>
    <a href="/binding">binding</a>
	<a href="/classesStyles">classesStyles</a>

</nav>





<br><br>
<div class="card">
<div class="cssColor fixedStyle marginCss" {onpointermove}>
	The pointer is at {Math.round(m.x)} x {Math.round(m.y)}
</div>


<!--  inline event handler 

<div
	onpointermove={(event) => {
		m.x = event.clientX;
		m.y = event.clientY;
	}}
>
	The pointer is at {Math.round(m.x)} x {Math.round(m.y)}
</div>


-->



<a href="./" class="homeLink">Home</a>

 
</div>

<div class="card2">
	<a href="./extracomponents" class="homeLink">Extra</a>
</div>

<!-- title    -->
<h1 class="titleEvents">Events</h1>





<br id="capture"><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div onkeydowncapture={(e) => alert(`<div> ${e.key}`)} role="presentation" style="margin-left: 1em;" class="marginLeft">
<label class="formatLabelEvent">order reversed</label>
	<input onkeydowncapture={(e) => alert(`<input> ${e.key}`)} class="marginLeft " />
</div>

<p class="styleIncrementDecrement">The current value is {value}</p>

<Stepper 
increment={() => value += 1} 
decrement={() => value -= 1}
/>

<div id="music" class="styleComponentBtn">
<BigButton onclick={hitit} /> 
</div>

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

<style>

      .titleEvents {
		   text-align: center;
	       margin-top: 2em;
		   margin-bottom: -4em;
	  }

	
	.fixedStyle {
			position: fixed;
			left: 0;
			top: 0;
			width: 20%;
			height: 20%;
			padding: 1rem;
			background-color: #36454F;
		
		}




	.cssColor {
		background-color: #476C9B;
	}

	.marginCss {
		margin-top: 15em;
		margin-left: 5em;
	}



	.homeLink {
		    
	        
	        text-align: center;
            font-family: 'Comic Sans MS', cursive;
            color: #00bcd4;
			

	}

	.onPointerStyle {
		font-size: 1.5em;
		font-family: 'Comic Sans MS', cursive;
		color: gray;
		text-align: center;
		margin-top: 4em;
		
	}

	 .card {
            background-color: #36454F; /* Light cyan color */
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            max-width: 300px;
			max-height: 100px;
            text-align: center;
			display: inline;
			
        }
       
		.card2 {
            background-color: #36454F; /* Light cyan color */
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            max-width: 300px;
			max-height: 100px;
            text-align: center;
			display: inline;
			
			
        }



	a {
	
		text-decoration: none;
	}

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

		.marginLeft {
			margin-left: 5%;
			display: inline;
			width: 100px;
		}


		.formatLabelEvent {
			font-size: 1.5em;
			font-family: 'Comic Sans MS', cursive;
			color: gray;
			text-align: center;
			margin-top: 4em;
			margin-left: 35%;
		}


		/* Media query for screens smaller than 600px */
       @media (max-width: 600px) {
           .formatLabelEvent {
           font-size: 18px;
           margin-left: .1%;
                 }
           
           

              }

			  @media (max-width: 450px) {
           .formatLabelEvent {
           font-size: 16px;
           margin-left: .1%;
                 }
           .marginLeft {

		           margin-left: 5%;
				   display: inline;
		           width: 70px;
		        }
		    }

			.styleIncrementDecrement {
				font-size: 1.5em;
				font-family: 'Comic Sans MS', cursive;
				color: gray;
				margin-left: 40%;
				margin-top: 4em;
			}

			.styleComponentBtn {

                margin-left: 40%;
				margin-top: 4em;
			}

</style>





