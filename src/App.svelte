<script>

let score = 0;
let result = ''
let result1 = ''
let result2 = ''
let result3 = ''

let first = ''
let second = ''
let third = ''
let forth = ''

let name = ''
let yes = ''
let no = ''

// CHECK BUTTON FUCTION (for multiple choice q's)
function check(a){
// if chosen answer has the value of 'one', answer = correct and point is added to the score.
  if (a.includes('one')){
    result = 'Correct !!'
    score += 1
// else if chosen answer doesnt have the value of 'one', answer = incorrect and no point is added.
  } else {
    result = 'Incorrect.'
}

//seperates each answer for each question.
if (a.includes('Q1')) {
			result1 = result
	} else if (a.includes('Q2')) {
			result2 = result
	} 
				
}

function confirm(b) { 
  if (name === 'one','1'){
    result3 = 'Correct !!'
    score += 1
  } else {
    result3 = 'Wrong.'
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

<h1>RUSSIAN LANGUAGE QUIZ</h1>

<br>

<!-- 1ST QUESTION - "How do you say..." -->
<h3>QUESTION 1:</h3>
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
<br>
<p> Score: {score} / 10</p>



<br>



<!-- QUESTION 2: -->
<h3>QUESTION 2:</h3>
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
<button on:click={check(second)}> Check </button>

{result2}
<br>
<p> Score: {score} / 10</p>




<br>




<h3>QUESTION 3:</h3>
<p>Which number is "A-deen" in English?</p>

<!-- <input id="question3" type="text"/> -->
<input type='text' bind:value={name} placeholder ='enter answer'>

<button on:click={confirm(name)}>Confirm</button> 
{result3}
<p> Score: {score} / 10</p>



<br>



<h3>QUESTION 4:</h3>
<p>True or False...?</p>

<!-- 
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