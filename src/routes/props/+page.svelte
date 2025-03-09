


<script>

    import Nestedx2 from './Nestedx2.svelte';

    import PackageInfo from './PackageInfo.svelte';

    import Nav from '.././Nav.svelte';

    

    const pkg = {
		name: 'svelte',
		version: 5,
		description: 'blazing fast',
		website: 'https://svelte.dev'
	};


    


</script>



<Nav />

<h1 class="titleProps">Props</h1>


<Nestedx2 answer={42} />
<Nestedx2 />



<PackageInfo {...pkg} />
<!-- <PackageInfo 
     name="svelte" 
     version="5" 
     description="blazing fast" 
     website="https://svelte.dev" /> -->





<footer>
     	<p>(Footer)  App created date:  March 02, 2025</p>
</footer>


<style>

.titleProps {
        color: black;
		font-family: 'Comic Sans MS', cursive;
		text-align: center;
        margin-bottom: 2em;
        margin-top: 1em;
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


