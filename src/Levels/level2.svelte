<script>
  let second = ''
</script>

<h3>Level 2 : Question 1</h3>
<p>How do you say red?</p>

<label>
	<input type='radio' bind:group={second} value='one'>
	A. "Gulaboi"
</label>

<label>
  <input type='radio' bind:group={second} value='two'>
	B. "Zillo-nyi"
</label>

<label>
  <input type='radio' bind:group={second} value='three'>
  C. "Krast-nyi"
</label>

{#if second === 'three'}
	<p>Correct!</p>
  <!-- Score:  -->
  {score =+1}
{:else if first === 'two'}
	<p>Incorrect, the answer was "Krast-nyi".</p>
  <!-- Score:  -->
  <!-- {score =-1} -->
 {:else if first === 'one'}
	<p>Incorrect, the answer was "Krast-nyi".</p>
  <!-- Score:  -->
  <!-- {score =-1} -->
{:else} 
  <p>Please choose an answer.</p>
{/if}