

<script>
    
     let name = $state('world');




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

        <br><br><br><br><br><br>