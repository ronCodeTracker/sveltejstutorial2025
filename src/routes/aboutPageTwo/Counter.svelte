


<script>
	import { counter } from './shared.svelte.js';
</script>

<button onclick={() => counter.count += 1}>
	clicks: {counter.count}
</button>



<style>

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
        
       



</style> 
