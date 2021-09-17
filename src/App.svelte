<script>

let score = 0;
let result = ''
let message = ''
let message1 = 'Thanks for playing!'

let first, second, third, forth, fifth, 
sixth, seventh, eighth, ninth, tenth = ''


let result1 = ''
let result2 = '' 
let result3 = ''
let result4 = ''
let result5 = ''
let result6 = ''
let result7 = ''
let result8 = ''
let result9 = ''
let result10 = ''



let name = ''
let name1 = ''
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
  } else if (a.includes('Q8')) {
      result8 = result
  }
}

// CHECK BUTTON FUNCTION (for text input q's)
function confirm(b) { 
  if (name === 'one'){
    result3 = 'Correct !!'
    score += 1
  } else {
    result3 = 'Wrong.'
  }
}

function confirm1(c) { 
  if (name1 === 'two'){
    result3 = 'Correct !!'
    score += 1
  } else {
    result3 = 'Wrong.'
  }
}

// while (score > 5) {
//   message = message1
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

<input type='text' bind:value={name} placeholder ='Enter a number'>

<button on:click={confirm(name)}>Confirm</button> 
{result3}
<p> Score: {score} / 10</p>



<br>



<h3>QUESTION 4:</h3>
<p>True or False, Privet is the informal what to say hello.</p>


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
<p>How do you say "How are you?" (formally) in Russian?</p>


<label>
	<input type='radio' bind:group={fifth} value='Q5two'>
	A. Kak Dela
</label>

<label>
  <input type='radio' bind:group={fifth} value='Q5one'>
	B. Kak Vashi Dela
</label>

<label>
  <input type='radio' bind:group={fifth} value='Q5three'>
  C. Kak Vashi
</label>

<p></p>
<button on:click={check(fifth)}> Check </button>

{result5}
<br>
<p> Score: {score} / 10</p>

<br>


<h3>QUESTION 6:</h3>
<p>Dratzvutyue means what in English?</p>


<label>
	<input type='radio' bind:group={sixth} value='Q6three'>
	A. Hi (Informal)
</label>

<label>
  <input type='radio' bind:group={sixth} value='Q6two'>
	B. Good Morning
</label>

<label>
  <input type='radio' bind:group={sixth} value='Q6one'>
  C. Hello (Formal)
</label>

<p></p>
<button on:click={check(sixth)}> Check </button>

{result6}
<p> Score: {score} / 10</p>

<br>


<h3>QUESTION 7:</h3>
<p>Which number is "Dva"?</p>

<input type='text' bind:value={name1} placeholder ='Enter a number'>

<button on:click={confirm1(name1)}>Confirm</button> 
{result7}
<p> Score: {score} / 10</p>

<br>


<h3>QUESTION 8:</h3>
<p>True or False, "Dobre Utra" means: Good Day?</p>

<label>
	<input type='radio' bind:group={eighth} value='Q8two'>
	True! 
</label>

<label>
	<input type='radio' bind:group={eighth} value='Q8one'>
	False! 
</label>
<br><br>
<button on:click={check(eighth)}> Check </button>
{result8}
<p> Score: {score} / 10</p>

<br>

<h3>QUESTION 9:</h3>
<p>"Das-va-dan-ya" mean what?</p>


<label>
	<input type='radio' bind:group={ninth} value='Q9two'>
	A. See you later
</label>

<label>
  <input type='radio' bind:group={ninth} value='Q9three'>
	B. Bye
</label>

<label>
  <input type='radio' bind:group={ninth} value='Q9one'>
  C. Goodbye
</label>

<br><br>
<button on:click={check(ninth)}> Check </button>
{result9}
<p> Score: {score} / 10 </p>

<br>


<h3>QUESTION 10:</h3>
<p>What does "Menya zavout (...)..." mean?</p>


<label>
	<input type='radio' bind:group={tenth} value='Q10one'>
	A. My name is (...)...
</label>

<label>
  <input type='radio' bind:group={tenth} value='Q10three'>
	B. I am (...)
</label>

<label>
  <input type='radio' bind:group={tenth} value='Q10two'>
  C. I'm from (...)
</label>

<br><br>
<button on:click={check(tenth)}> Check </button>
{result10}
<p> Score: {score} / 10 </p>

<br>

<h3>{message}</h3>