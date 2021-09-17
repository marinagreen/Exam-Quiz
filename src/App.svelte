<script>

// Score & Result output
let score = 0;
let result = ''


// category for each question
let first, second, third, forth, fifth, 
sixth, seventh, eighth, ninth, tenth = ''

// result output for each answer
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


// Text Questions and True or False Outputs
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

// CHECK BUTTON FUNCTIONS (for text input q's)
// question 3 code.
function confirm(b) { 
  if (name === 'one'){
    result3 = 'Correct !!'
    score += 1
  } else if (name === '1'){
    result3 = 'Correct !!'
    score += 1
  } else {
    result3 = 'Wrong.'
  }
}

//question 7 code
function confirm1(c) { 
  if (name1 === 'two'){
    result3 = 'Correct !!'
    score += 1
  } else if (name === '2'){
    result3 = 'Correct !!'
    score += 1
  } else {
    result3 = 'Wrong.'
  }
}


</script>

<h1>RUSSIAN LANGUAGE QUIZ</h1>

<br>

<!-- 1ST QUESTION - "How do you say..." -->
<h3>QUESTION 1:</h3>
<p>How do you say "one" / "1" in Russian?</p>

<!-- Correct Answer -->
<label>
	<input type='radio' bind:group={first} value='Q1one'>
	A. "A-deen"
</label>

<!-- False Answer -->
<label>
  <input type='radio' bind:group={first} value='Q1two'>
	B. "Voy-shem"
</label>

<!-- False Answer -->
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



<!-- QUESTION 2: Russian to English -->
<h3>QUESTION 2:</h3>
<p>Which number is "Voy-shem" in English?</p>

<label>
	<input type='radio' bind:group={second} value='Q2two'>
	A. "5"
</label>

<!-- Correct Answer -->
<label>
  <input type='radio' bind:group={second} value='Q2one'>
	B. "8"
</label>

<!-- False Answer -->
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

<!-- Correct Answer is "1" or "One" -->
<input type='text' bind:value={name} placeholder ='Enter a number'>

<button on:click={confirm(name)}>Confirm</button> 
{result3}
<p> Score: {score} / 10</p>



<br>



<h3>QUESTION 4:</h3>
<p>True or False, Privet is the informal what to say hello.</p>

<!-- Correct Answer -->
<label>
	<input type='radio' bind:group={forth} value='Q4one'>
	True! 
</label>

<!-- False Answer -->
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

<!-- False Answer -->
<label>
	<input type='radio' bind:group={fifth} value='Q5two'>
	A. Kak Dela
</label>

<!-- Correct Answer -->
<label>
  <input type='radio' bind:group={fifth} value='Q5one'>
	B. Kak Vashi Dela
</label>

<!-- False Answer -->
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

<!-- False Answer -->
<label>
	<input type='radio' bind:group={sixth} value='Q6three'>
	A. Hi (Informal)
</label>

<!-- False Answer -->
<label>
  <input type='radio' bind:group={sixth} value='Q6two'>
	B. Good Morning
</label>

<!-- Correct Answer -->
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

<!-- Correct Answer is "Two" or "2" -->
<input type='text' bind:value={name1} placeholder ='Enter a number'>

<button on:click={confirm1(name1)}>Confirm</button> 
{result7}
<p> Score: {score} / 10</p>


<br>


<h3>QUESTION 8:</h3>
<p>True or False, "Dobre Utra" means: Good Day?</p>

<!-- False Answer -->
<label>
	<input type='radio' bind:group={eighth} value='Q8two'>
	True! 
</label>

<!-- Correct Answer -->
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

<!-- False Answer -->
<label>
	<input type='radio' bind:group={ninth} value='Q9two'>
	A. See you later
</label>

<!-- False Answer -->
<label>
  <input type='radio' bind:group={ninth} value='Q9three'>
	B. Bye
</label>

<!-- Correct Answer -->
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

<!-- Correct Answer -->
<label>
	<input type='radio' bind:group={tenth} value='Q10one'>
	A. My name is (...)...
</label>

<!-- False Answer -->
<label>
  <input type='radio' bind:group={tenth} value='Q10three'>
	B. I am (...)
</label>

<!-- False Answer -->
<label>
  <input type='radio' bind:group={tenth} value='Q10two'>
  C. I'm from (...)
</label>

<br><br>
<button on:click={check(tenth)}> Check </button>
{result10}
<p> Score: {score} / 10 </p>


<br>


<h3>Thanks for Playing!</h3>