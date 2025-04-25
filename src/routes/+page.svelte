


<!--

Name:  Ronald Kiefer
Date:  February 26, 2025  Wednesday



-->


<script>
	
	import Header from './Header.svelte';

    import Nested from './Nested.svelte';

    import aboutPageTwo from './aboutPageTwo/+page.svelte';

    import Nav from './NavG.svelte';



    

	let formState = $state({
		name: '',
		birthday: '',
		step: 0,
		error: ''
	})


    let src = 'https://giphy.com/embed/Vuw9m5wXviFIQ';
	let name = 'Rick Astley';

    



</script>




<Header name={formState.name} />





<Nav />


<main>
<container>

{#if formState.name }<h1>{formState.name}'s Form</h1>
{/if}
<p class="centerParagraph colorBrown">Step: {formState.step + 1}</p>



 {#if formState.step === 0}
    <div class="centerInput"> 
		<div class="after"><label class="inlineDisplay" for="name">Name:</label></div>
		<div class="after"><input class="inlineDisplay" type="text" id="name" bind:value={formState.name} /></div>
       
	</div>
	<button onclick={() => { if(formState.name !== "") 
	{formState.step += 1;
	formState.error = '';
	} else {
	formState.error = "Name is required";
    }}

    }>Next</button>


	{:else if formState.step === 1}
	    <div class="formRight"> 
		   <label for="bday">Your Birthday</label>
		   <input type="date" id="bday" bind:value={formState.birthday} />
	    </div>
	  <button onclick={() => { if(formState.birthday !== "") 
	    {formState.step += 1;
	    formState.error = '';
	    } else {
	      formState.error = "Birthday is required";
        }}

    }>Next</button>


    
 {/if}

 {#if formState.error}
    <p class="error">Error!&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{formState.error}</p>
{/if}

 <div></div>


 <a href="/events" class="anchorMain">main</a>


 <br>
 <iframe {src} width="100" height="100" style=""  frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

 








</container>
</main>


<style>

    .error {
            
        color: red;
			margin-bottom: 20px;
			margin-left: 10px;

    }


	main {
	    	font-family: Arial, sans-serif;
            background-color: lightgray;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 130vh;
	}

	container {
		    background-color: #ffffff;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 20em;
           
	}

	h1 {
            color: #388e3c;
            margin-bottom: 20px;
    }

	.colorBrown {
            color: brown;
            margin-bottom: 20px;
    }


    .inlineDisplay {
        display: inline;
    }
    .centerInput {
        margin: 0 auto;
        width: 70%;
    }


    .centerParagraph {
        margin: 0 auto;
        width: 70%;
        margin-bottom: 20px;
    }

	input[type="text"] {
            
            padding: 10px;
            width: 10em;
            margin-bottom: 20px;
            margin-left: 10px;
            
            border: 1px solid #a5d6a7;
            border-radius: 4px;
        }

	  button {
            padding: 10px 20px;
            background-color: #66bb6a;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            margin-top: 20px;
        }


      button:hover {
            background-color: #388e3c;
        }

        div.after {
          display: inline;
       }


       
	        :global(.comicStyle) {
		        color: goldenrod;
		        font-family: 'Comic Sans MS', cursive;
		        font-size: 1.2em;
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
             
        .anchorMain {
            float: right;
            text-align: center;
            font-family: 'Comic Sans MS', cursive;
            color: chartreuse;
            text-decoration: none;
            border: 1px solid #a5d6a7;
            border-radius: 8px;
            padding: 10px;

        }

</style>







