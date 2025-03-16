

<script>
    
     let name = $state('world');

     let a = $state(3);
	 let b = $state(3);

     //check box binding
     let yes = $state(false);

     let questions = $state([
		{
			id: 1,
			text: `Where did you go to school?`
		},
		{
			id: 2,
			text: `What is your mother's name?`
		},
		{
			id: 3,
			text: `What is another personal fact that an attacker could easily find with Google?`
		}
	]);

    let selected = $state();

	let answer = $state('');

	function handleSubmit(e) {
		e.preventDefault();

		alert(
			`answered question ${selected.id} (${selected.text}) with "${answer}"`
		);
	}



</script>




<style>
    body {
        font-family: 'Arial', sans-serif;
        background-color: #f5f5f5;
        margin: 0;
        padding: 0;
        box-sizing: border-box;
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


    .container {
        background-color: #efe7df;
        padding: 30px;
        padding-top: 5px;
        border-radius: 10px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        max-width: 800px;
        margin: 20px auto;
        margin-left: 15%;
        margin-right: 15%;
        margin-top: 2em;
        text-align: center;
    }



h1 {
        font-size: 36px;
        color: #333333;
        margin-bottom: 20px;
        position: relative;
    }
    

        p {
        font-size: 18px;
        color: #666666;
        line-height: 1.6;
        margin: 0;
    }

    .widthStyle {
		width: 70%;
		margin: 0 auto;
	
    }


.textboxInputStyle {
		width: 20%;
		padding: 10px;
		margin: 10px 30px;
        margin-top: 30px;
		border: 1px solid #ccc;
		border-radius: 4px;
		font-size: 16px;
		box-sizing: border-box;
	}

    .outputStyle {
		font-size: 20px;
		color: #333333;
		margin: 2px 20%;
        margin-bottom: 3em;
        margin-top: 2em;
	}

    .label-container {
		display: flex;
		gap: 10em; /* Space between the input items */
        padding: 20px;
        margin-bottom: 2em;
	}


    .input-container {
        display: inline;
        margin-right: 50px;
       

    }

    .input-container-2 {
		display: inline;
		
	}


    .textbox-1 {
        margin-bottom: 20%;
    }


    
    .textboxlabel-2 {

        margin-right: 50px;
        margin-bottom: 20%;
    }


    .paragraphOutput {
        margin-left: 20%;
    }


    input[type="range"] {
    -webkit-appearance: none;
    width: 50%;
    height: 6px;
    background: #ddd;
    border-radius: 5px;
    outline: none;
    transition: background 0.3s;
}

input[type="range"]::-webkit-slider-thumb {
    -webkit-appearance: none;
    appearance: none;
    width: 15px;
    height: 15px;
    background: #04724D; /*  green color */
    border-radius: 50%;
    cursor: pointer;
    box-shadow: 0 0 5px rgba(50, 205, 50, 0.5);
    transition: background 0.3s, transform 0.3s;
    position: relative;
    top: -4.5px; /* Adjust thumb position */
}

input[type="range"]::-moz-range-thumb {
    width: 15px;
    height: 15px;
    background: #32CD32; /* Lime green color */
    border-radius: 50%;
    cursor: pointer;
    box-shadow: 0 0 5px rgba(50, 205, 50, 0.5);
    transition: background 0.3s, transform 0.3s;
    position: relative;
    top: -4.5px; /* Adjust thumb position */
}


input[type="range"]::-webkit-slider-runnable-track {
    width: 100%;
    height: 6px;
    cursor: pointer;
    background: linear-gradient(to right, #006400, #00FF7F); /* Green gradient */
    border-radius: 5px;
}


input[type="range"]::-moz-range-track {
    width: 100%;
    height: 6px;
    cursor: pointer;
    background: linear-gradient(to right, #006400, #00FF7F); /* Green gradient */
    border-radius: 5px;
}


input[type="range"]:hover::-webkit-slider-thumb {
    background: #00FF7F; /* Light green color */
    transform: scale(1.2);
}

input[type="range"]:hover::-moz-range-thumb {
    background: #00FF7F; /* Light green color */
    transform: scale(1.2);
}


.containerForCard {
    background-color: #ADD9F4;
    margin-bottom: 5em;
    padding-bottom: 5em;
    padding-top: 5em;
}


.card {
    background-color: #ffffff;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    padding: 20px;
    max-width: 300px;
    text-align: center;
    margin-left: 10%;
}


.format-title-bindingSelect {
	margin-left: 15%;
	color: orange;
    color: #E58F65;
}


.format-title-bindingSelect2 {
    margin-left: 1em;
    display: block;
}

.format-answer-bindingSelect {
	margin-left: 1em;
	margin-top: 1em;
	margin-bottom: 1em;
    margin-right: 1em;
	display: inline;
}

.format-text-binding {
	margin-left: 15%;
	margin-top: 1em;
	margin-bottom: 1em;
	margin-right: 1em;
	
    color: #E58F65;
    
    
}


</style>


 

<nav>
	<a href="/events">main</a>
	<a href="/events/#music">music</a>
    <a href="/binding">binding</a>
</nav>



<div class="container">
    <h1>Bindings</h1>
    <p class="widthStyle">We will first study and use the textbox binding (Text inputs bindings)
with the bind:value= &#123;name&#125; format.</p>
</div>


        <input bind:value={name} class="textboxInputStyle" />
        <h1 class="outputStyle">Hello {name}!</h1>

        <hr>

        <br><br><br>
        

        <div class="label-container">

        <label>
            <div class="input-container">
	        <input type="number" bind:value={a} min="0" max="10" class="textbox-1" />
	        </div>
            <div class="input-container-2">
            <input type="range" bind:value={a} min="0" max="10" />
            </div>      
        </label>

        <label>
	        <input type="number" bind:value={b} min="0" max="10" class="textboxlabel-2" />
	        <input type="range" bind:value={b} min="0" max="10" />
        </label>

        </div>

  <p class="paragraphOutput">{a} + {b} = {a + b}</p>

        
        
        <br><br><br>
<div class="containerForCard">
<div class="card">
<label>
	<input type="checkbox" bind:checked={yes} />
	Yes! Send me regular email spam
</label>

<br><br><br>




{#if yes}
	<p>
		Thank you. We will bombard your inbox and sell
		your personal details.
	</p>
{:else}
	<p>
		You must opt in to continue. If you're not
		paying, you're the product.
	</p>
{/if}

<br><br><br>


<button disabled={!yes}>Subscribe</button>

</div>
</div>


        <br><br><br>

<h2 class="format-title-bindingSelect">Insecurity questions</h2>


<form onsubmit={handleSubmit}>
	<select
		bind:value={selected}
		onchange={() => (answer = '')}
        class="format-title-bindingSelect2"
	>
		{#each questions as question}
			<option value={question}>
				{question.text}
			</option>
		{/each}
	</select>


<input bind:value={answer} class="format-answer-bindingSelect" />


<button disabled={!answer} type="submit">
		Submit
	</button>
</form>



<p class="format-text-binding">
	selected question {selected
		? selected.id
		: '[waiting...]'}
</p>



<br><br><br><br><br><br>


