

<script>
	let { name, version, description, website } = $props();
</script>


<div class="mainCard">
     <div class="card">
    
    <p>The { name } package is blazing fast. 
    Download version { version } from
    <a href="https://www.npmjs.com/package/{name}">npm</a> 
    and <a href={website}>learn more.</a></p>    

    </div>

</div>

<style>

    p, code {
	font-family: Verdana, sans-serif;
    }

	.mainCard {
            font-family: Arial, sans-serif;
            background-color: #f5f5f5;
            display: flex;
            justify-content: left;
            align-items: center;
            height: 30vh;
            margin: 0;
            margin-top: 25px;
            
            padding-bottom: 10em;
        }


  .card {
            background-color: #ADD9F4; /* Vibrant yellow color */
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            max-width: 400px;
            text-align: center;
            margin-left: 15%;
        }

        .card p {
            color: #333;
            font-size: 16px;
            margin: 0;
        }

        .card a {
            color: #388e3c; /* Green color for links */
            text-decoration: none;
            font-weight: bold;
        }
        .card a:hover {
            text-decoration: underline;
        }


</style>


