
<script>

   import Counter from './Counter.svelte';

   import Nav from '.././NavG.svelte';


   let elapsed = $state(0);
   let interval = $state(1000);

   $effect(() => {
	   const id = setInterval(() => {
		   elapsed += 1;
	   }, interval);

	   return () => clearInterval(id);
   });



</script>





<Nav />

<h1 class="titleAboutTwo">About Page Two</h1>

<!--    
<p class="aboutPageStyle">This Is The About Page Two</p>
-->


<p class="timePg">ELAPSED:  &nbsp;&nbsp; {elapsed}</p>



<button onclick={() => interval /= 2}>speed up</button>
<button onclick={() => interval *= 2}>slow down</button> 

<button onclick={() => elapsed = 0} class="buttonTweek">reset</button>
<br><br><br>
<div class="displayChangePlus">&nbsp;&nbsp;&nbsp;&nbsp;</div><Counter />
<div class="displayChange"></div>
<Counter />
<Counter />

<footer>
     	<p>(Footer)  App created date:  March 02, 2025</p>
</footer>


<div class="marginSpan"></div>








<style>

     .titleAboutTwo {
        color: black;
		font-family: 'Comic Sans MS', cursive;
		text-align: center;
        margin-bottom: 2em;
        margin-top: 1em;
     }




     nav {
            background-color: #388e3c;
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
            background-color: #66bb6a;
        }


 


        button{
            padding: 10px 20px;
            background-color: #8B4513;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            margin-top: 20px;            
            display: block;
            margin-left: 9.3em;
            width: 170px;
        }

        button:hover {
            background-color: #A0522D;
        }

        button:active {
            background-color: #5C4033;
            transform: scale(1);
        }


        .timePg {
            margin-left: 5em;
            font-size: 1.5em;
        }

        .buttonTweek {
            width: 60px;
            background-color: #555555;
            padding: 5px 10px;            
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            margin-top: 30px;            
            display: block;
            margin-left: 17.3em;
            
        }

        .buttonTweek:hover {
            background-color: #777777;
        }

        .buttonTweek:active {
            background-color: #333333;
            transform: scale(1);
        }


        .displayChangePlus {
            display: inline;
            margin-left:10%;
        }

        .displayChange {
            display: inline;
        }

        .marginSpan {
            margin-bottom: 10em;
        }


        footer {
            
			background-color: #42a5f5;
			color: white;
			text-align: center;
			padding: 10px 20px;
			position: fixed;
			bottom: 0;
			width: 100%;
        }



</style>


