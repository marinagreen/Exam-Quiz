<script>
// import resources from './Resource.svelte';
// import level1questions from './level1.svelte';
let score = 0;
let level = ''
let first = ''
let second = ''
let third = ''
let name = ''

//  function btnCheck() {
//   {#if level === 'easy'}
// 	  {level1questions}
//  {:else if level === 'medium'}
// 	  {level2questions}
// {:else if first === 'hard'}
//  	{level3questions}
// {:else} 
//    <p>Please choose a level.</p>
// {/if}
//  }


function btnConfirm1() {
 {#if name === 'one'}
	<p>Incorrect, the answer was "8".</p>
{:else if name === 'two'}
	<p>Correct!</p>
   Score: {score+1}
 {:else if name === 'three'}
	<p>Incorrect, the answer was "8".</p>
{:else} 
  <p>Please choose an answer.</p>
{/if} 
}


</script>

<!-- Choose Level, e.g. 1,2,3, > resource page for the level shows, once ready begin -->
<h3>Select Your Level</h3>

<select name="level" id="level">
  <option value="easy">Easy</option>
  <option value="medium">Medium</option>
  <option value="hard">Hard</option>
</select>

<!-- Select level button
<!-- <button on:click={btnCheck}>
	Confirm
</button> --> 

<!--Btn start, gets rid of resouce page, shows first question, once answered, removes question and shows the next question, repeats until ten questions.-->

<h3> -- </h3>


<!-- 1ST QUESTION - "How do you say..." -->
<h3>Level 1 : Question 1</h3>
<p>How do you say "one" / "1" in Russian?</p>

<label>
	<input type='radio' bind:group={first} value='one'>
	A. "A-deen"
</label>

<label>
  <input type='radio' bind:group={first} value='two'>
	B. "Voy-shem"
</label>

<label>
  <input type='radio' bind:group={first} value='three'>
  C. "Dva"
</label>

{#if first === 'one'}
	<p>Correct!</p>
  Score: {score=+1}
{:else if first === 'two'}
	<p>Incorrect, the answer was "A-deen".</p>
 {:else if first === 'three'}
	<p>Incorrect, the answer was "A-deen".</p>
{:else} 
  <p>Please choose an answer.</p>
{/if}


<!-- QUESTION 2: -->
<h3>Level 1 : Question 2</h3>
<p>Which number is "Voy-shem" in English?</p>

<label>
	<input type='radio' bind:group={second} value='one'>
	A. "5"
</label>

<label>
  <input type='radio' bind:group={second} value='two'>
	B. "8"
</label>

<label>
  <input type='radio' bind:group={second} value='three'>
  C. "3"
</label>

{#if second === 'one'}
	<p>Incorrect, the answer was "8".</p>
{:else if second === 'two'}
	<p>Correct!</p>
   Score: {score+1}
 {:else if second === 'three'}
	<p>Incorrect, the answer was "8".</p>
{:else} 
  <p>Please choose an answer.</p>
{/if}


<h3>Level 1 : Question 3</h3>
<p>Which number is "A-deen" in English?</p>

<!-- <input id="question3" type="text"/> -->
<input id="question3" value={name}>

<button on:click={btnConfirm1}>
	Confirm
</button> 

<!-- {#if question3 === 'one'}
	<p>Incorrect, the answer was "8".</p>
{:else if question3 === 'two'}
	<p>Correct!</p>
   Score: {score+1}
 {:else if question3 === 'three'}
	<p>Incorrect, the answer was "8".</p>
{:else} 
  <p>Please choose an answer.</p>
{/if} -->


