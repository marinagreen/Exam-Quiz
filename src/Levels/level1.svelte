<script>
let first = ''
</script>


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
  <!-- Score:  -->
  {score =+1}
{:else if first === 'two'}
	<p>Incorrect, the answer was "A-deen".</p>
  <!-- Score:  -->
  <!-- {score =-1} -->
 {:else if first === 'three'}
	<p>Incorrect, the answer was "A-deen".</p>
  <!-- Score:  -->
  <!-- {score =-1} -->
{:else} 
  <p>Please choose an answer.</p>
{/if}
