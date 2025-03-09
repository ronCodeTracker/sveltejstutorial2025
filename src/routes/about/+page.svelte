
 <script>
    import Nested from '../Nested.svelte';

    import Nav from '.././NavG.svelte';

	let string = 'This is a good <strong>Day!</strong>';


 </script>




<Nav />

<h1 class="aboutStyle">about</h1>
<p class="aboutPageStyle">This Is The About Page</p>

<p class="comicStyle paragraph">This is a paragraph.</p>


<Nested />


<p class="paragraph">{@html string}</p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


    <footer>
     	<p>(Footer)  App created date:  February 28, 2025</p>
    </footer>

<style>

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

        .aboutStyle {
			color: red;
            font-family: 'Comic Sans MS', cursive;
            text-align: center;
		}


        .aboutPageStyle {
            text-align: center;
            font-family: 'Comic Sans MS', cursive;
            color: brown;
        }


        .paragraph {
            margin-left: 30px;
        }

        footer {
            
			background-color: #388e3c;
			color: white;
			text-align: center;
			padding: 10px 20px;
			position: fixed;
			bottom: 0;
			width: 100%;
        }
</style>
