

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
        background-color: #ffffff;
        padding: 30px;
        border-radius: 10px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        max-width: 800px;
        margin: 20px auto;
        text-align: center;
    }



h1 {
        font-size: 36px;
        color: #333333;
        margin-bottom: 20px;
        position: relative;
    }
    h1::after {
        content: '';
        width: 50px;
        height: 4px;
        background-color: #ff6347; /* Tomato color */
        position: absolute;
        bottom: -10px;
        left: 50%;
        transform: translateX(-50%);
        border-radius: 2px;
    }

        p {
        font-size: 18px;
        color: #666666;
        line-height: 1.6;
        margin: 0;
    }
</style>


 

<nav>
	<a href="/events">main</a>
	<a href="/events/#music">music</a>
    <a href="/binding">binding</a>
</nav>



<div class="container">
    <h1>Interesting Title</h1>
    <p>This is a single paragraph with an interesting style. The title has a decorative underline, and the paragraph text is styled for readability.</p>
</div>