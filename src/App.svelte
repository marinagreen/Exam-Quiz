<script>
// import resources from './Resource.svelte';
// import level1questions from './level1.svelte';
let score = 0;
let level = ''
// let first = ''
// let second = ''
//let third = ''

//  function btnCheck() {
//   {#if level === 'easy'}
// 	{level1questions}
// {:else if level === 'medium'}
// 	{level2questions}
// {:else if first === 'hard'}
// 	{level3questions}
// {:else} 
// <p>Please choose a level.</p>
// {/if}
//  }

// function Level() {
// 	// <p>{score}</p>
// }
</script>

<!-- Choose Level, e.g. 1,2,3, > resource page for the level shows, once ready begin -->
<!--Btn start, gets rid of resouce page, shows first question, once answered, removes question and shows the next question, repeats until ten questions.-->

<!-- IDEA - add a hint button?? -->

<!-- 1ST QUESTION - "How do you say..." -->

<!-- Select level button -->

<h3>Select Your Level</h3>



<select name="level" id="level">
  <option value="easy">Easy</option>
  <option value="medium">Medium</option>
  <option value="hard">Hard</option>
</select>

<button on:click={btnCheck}>
	Confirm
</button>