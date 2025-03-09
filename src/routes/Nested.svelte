

<!--

Name:  Ronald Kiefer
Date:  February 27, 2025  Thursday
Course:  Svelte 5 docs tutorial
Web:  svelte.dev


-->


<script>

//import aboutTwo from './about/+page.svelte';


let count = $state(0);

function increment() {
    count += 1;
}


//  Deep state
let numbers = $state([1, 2, 3, 4]);
let total = $derived(numbers.reduce((t, n) => t + n, 0));
let numbers2 = $state([1, 2, 3, 4]);
let total2 = $derived(numbers2.reduce((t, n) => t + n, 0));


function addNumber() {
		numbers.push(numbers.length + 1);
        console.log($state.snapshot(numbers));
	}


function addNumber2() {
		numbers2.push(numbers2.length + 1);
        console.log($state.snapshot(numbers2));
	}


    //let { answer } = $props();

    //export const answer = $state(42);


    


</script>


<p class="paragraph">This is another paragraph.</p>

<button onclick={increment} class="buttonTimes">Clicked {count}
{count === 1 ? 'time' : 'times'}
</button>

<p>{numbers.join(' + ')} = </p>



<button onclick={addNumber} class="button2Times">
	Add a number
</button>

<p>{numbers2.join(' + ')} = {total2}</p>

<button onclick={addNumber2} class="button3Times">
	Add a number
</button>



<style>

  .paragraph {
            margin-left: 30px;
        }


   .buttonTimes {


        margin-left: 30%;
        width: 10em;
        padding: 10px 20px;
        background-color: #555555;
        color: #fff;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        font-size: 16px;
        transition: background-color 0.3s, transform 0.3s;
   }

    .buttonTimes:hover {
            background-color: #777777;
            transform: scale(1.05);
        }
    .buttonTimes:active {
            background-color: #333333;
            transform: scale(1);
        }




    .button2Times {


        margin-left: 30%;
        width: 10em;
        padding: 10px 20px;
        background-color: #8B4513;
        color: #fff;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        font-size: 16px;
        transition: background-color 0.3s, transform 0.3s;
   }



   .button2Times:hover {
            background-color: #A0522D;
            transform: scale(1.05);
        }
    .button2Times:active {
            background-color: #5C4033;
            transform: scale(1);
        }


    .button3Times {


        margin-left: 30%;
        width: 10em;
        padding: 10px 20px;
        background-color: #555555;
        color: #fff;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        font-size: 16px;
        transition: background-color 0.3s, transform 0.3s;
   }



   .button3Times:hover {
            background-color: #777777;
            transform: scale(1.05);
        }
    .button3Times:active {
            background-color: #333333;
            transform: scale(1);
        }


</style>