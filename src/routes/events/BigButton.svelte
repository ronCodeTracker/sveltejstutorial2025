


<script>
	let props = $props();
</script>


<button class="button" {...props}><i class="fas fa-music"></i>
	Push
</button>


<style>
     
        @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css');


       .button {
            padding: 15px 30px;
            background-color: #8B4513; /* Brown color */
            color: #ffffff;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            font-size: 20px;
            font-weight: bold;
            transition: background-color 0.3s, transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        .button i {
            margin-right: 10px;
        }
        .button:hover {
            background-color: #A0522D; /* Lighter brown */
            transform: scale(1.05);
            box-shadow: 0 6px 8px rgba(0, 0, 0, 0.2);
        }
        .button:active {
            background-color: #5C4033; /* Darker brown */
            transform: scale(1);
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

</style>
