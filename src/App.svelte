<script>
// import resources from './Resource.svelte';
// import level1questions from './level1.svelte';

let score = 0;
let result = ''
// let level = ''

let first = ''
let second = ''
let third = ''
let forth = ''

let name = ''
let yes = ''
let no = ''
let result1=''
let result2=''

// SELECT LEVEL FUNCTION
// function btnCheck() {
// if (level === ('easy')){
// //     level1questions
// } else if (level === ('medium')){
// // 	   level2questions
// } else if (level === ('hard')){
// //     level3questions
// } else {
//         'Please choose a level.'
// }}

// CHECK BUTTON FUCTION (for multiple choice q's)
function check(a){
  if (a.includes('one')){
    result = 'Correct'
    score += 1
  } else {
    result = 'Wrong'
  }

  	if (a.includes('Q1')) {
				result1 = result
		} else if (a.includes('Q2')) {
				result2 = result
		} 
				
}



// CHECK BUTTON FUNCTION (for text input q's)
// function btnConfirm1() {
//  if (name === 'one')
//  result = 'Correct!'
//  score =+1
// } else {
//   result = 'Wrong."'
// }

</script>

<!-- CHOOSE LEVEL 1,2, OR 3. SHOWS RESOURCE AND QUESTIONS BASED ON YOUR ANSWER. -->
<!-- <h3>Select Your Level</h3>

<select name="level" id="level">
  <option value="easy">Easy</option>
  <option value="medium">Medium</option>
  <option value="hard">Hard</option>
</select>

<!-- SELECT LEVEL BUTTON -->
<!-- <button on:click={btnCheck}>
	Confirm
</button>  --> -->

<!--BTN STARTS, REMOVES RESOURCES, SHOWS FIRST QUESTION, ONCE ANSWERED, REMOVES QUESTION & SHOWS NEXT QUESTION, REPEATS.-->




<h3> --------------------------------- </h3>


<!-- 1ST QUESTION - "How do you say..." -->
<h3>Level 1 : Question 1</h3>
<p>How do you say "one" / "1" in Russian?</p>


<label>
	<input type='radio' bind:group={first} value='Q1one'>
	A. "A-deen"
</label>

<label>
  <input type='radio' bind:group={first} value='Q1two'>
	B. "Voy-shem"
</label>

<label>
  <input type='radio' bind:group={first} value='Q1three'>
  C. "Dva"
</label>

<p></p>
<button on:click={check(first)}> Check </button>

{result1}



<h3> --------------------------------- </h3>



<!-- QUESTION 2: -->
<h3>Level 1 : Question 2</h3>
<p>Which number is "Voy-shem" in English?</p>

<label>
	<input type='radio' bind:group={second} value='Q2two'>
	A. "5"
</label>

<label>
  <input type='radio' bind:group={second} value='Q2one'>
	B. "8"
</label>

<label>
  <input type='radio' bind:group={second} value='Q2three'>
  C. "3"
</label>

<p></p>
<button on:click={check(first)}> Check </button>

{result2}

<h3> --------------------------------- </h3>





<h3>Level 1 : Question 3</h3>
<p>Which number is "A-deen" in English?</p>

<!-- <input id="question3" type="text"/> -->
<input id="third" value={name}>

<button on:click={btnConfirm1}>
	Confirm
</button> 


<!-- <h3> --------------------------------- </h3>

<h3>Level 1 Question 4</h3>
<p>True or False...?</p>


<label>
	<input type='radio' bind:group={forth} value='yes'>
	True! 
</label>

<label>
	<input type='radio' bind:group={forth} value='no'>
	False! 
</label>

{#if forth === yes}
	<p>Correct!</p>
{:else if forth === no}
	<p>Incorrect!</p>
  {:else}
  <p>Please choose an answer.</p>
{/if}

<p></p>

<button on:click={btnConfirm2}>
	Confirm
</button>  -->