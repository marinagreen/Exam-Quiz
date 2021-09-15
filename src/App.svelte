<script>

let score = 0;
let result = ''

let first = ''
let second = ''
let third = ''
let forth = ''
let fifth = ''
let sixth = ''

let result1 = ''
let result2 = ''
let result3 = ''
let result4 = ''
let result5 = ''
let result6 = ''

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
	} else if (a.includes('Q4')) {
      result4 = result
  } else if (a.includes('Q5')) {
      result5 = result
  } else if (a.includes('Q6')) {
      result6 = result
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
<input type='text' bind:value={name} placeholder ='Enter a number'>

<button on:click={confirm(name)}>Confirm</button> 
{result3}
<p> Score: {score} / 10</p>



<br>



<h3>QUESTION 4:</h3>
<p>True or False, (Enter Question Here)?</p>


<label>
	<input type='radio' bind:group={forth} value='Q4one'>
	True! 
</label>

<label>
	<input type='radio' bind:group={forth} value='Q4two'>
	False! 
</label>

<p></p>

<button on:click={check(forth)}>Check</button>
{result4}
<p> Score: {score} / 10</p>

<br>

<h3>QUESTION 5:</h3>
<p>Placeholder</p>


<label>
	<input type='radio' bind:group={fifth} value='Q5two'>
	A. Wrong
</label>

<label>
  <input type='radio' bind:group={fifth} value='Q5one'>
	B. Right
</label>

<label>
  <input type='radio' bind:group={fifth} value='Q5three'>
  C. Wrong
</label>

<p></p>
<button on:click={check(fifth)}> Check </button>

{result5}
<br>
<p> Score: {score} / 10</p>

<br>


<h3>QUESTION 6:</h3>
<p>Placeholder</p>


<label>
	<input type='radio' bind:group={sixth} value='Q6three'>
	A. Wrong
</label>

<label>
  <input type='radio' bind:group={sixth} value='Q6two'>
	B. Wrong
</label>

<label>
  <input type='radio' bind:group={sixth} value='Q6one'>
  C. Right
</label>

<p></p>
<button on:click={check(sixth)}> Check </button>

{result6}
<p> Score: {score} / 10</p>

<br>


<!-- <h3>QUESTION 7:</h3>
<p>Placeholder</p>

<!-- <input id="question3" type="text"/> -->
<!-- <input type='text' bind:value={name} placeholder ='Enter a number'>

<button on:click={confirm1(name)}>Confirm</button> 
{result7}
<p> Score: {score} / 10</p> --> -->