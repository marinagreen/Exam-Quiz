<script>
  let third = ''
</script>

<h3>Level 3 : Question 1</h3>
<p>How do you say hello (formal)?</p>

<label>
	<input type='radio' bind:group={third} value='one'>
	A. "Privet"
</label>

<label>
  <input type='radio' bind:group={third} value='two'>
	B. "Dratzvutyre"
</label>

<label>
  <input type='radio' bind:group={third} value='three'>
  C. "Kak dela"
</label>


{#if third === 'two'}
	<p>Correct!</p>
  <!-- Score:  -->
  {score =+1}
{:else if first === 'three'}
	<p>Incorrect, the answer was "Dratzvutyre".</p>
  <!-- Score:  -->
  <!-- {score =-1} -->
 {:else if first === 'one'}
	<p>Incorrect, the answer was "Dratzvutyre".</p>
  <!-- Score:  -->
  <!-- {score =-1} -->
{:else} 
  <p>Please choose an answer.</p>
{/if}