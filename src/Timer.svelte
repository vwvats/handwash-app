<script>
  import { createEventDispatcher } from 'svelte';
  import ProgressBar from './ProgressBar.svelte';

  const totalTime = 20;
  let secondsLeft = totalTime;
  let isRunning = false;
  $: progress = ((totalTime - secondsLeft) / totalTime) * 100;
  const dispatch = createEventDispatcher();

  function startTimer() { 
    isRunning = true;
    const timer = setInterval( () => {
      secondsLeft -= 1;
      if (secondsLeft == 0) {
        clearInterval(timer);
        isRunning = false;
        secondsLeft = totalTime;
        dispatch('end');
      }
    }, 1000);
  }
</script>

<div bp="grid">
  <h2 bp="offset-4@md 6@md 12@sm">Seconds Left : {secondsLeft}</h2>
</div>

<ProgressBar {progress} />

<div bp="grid">
  <button bp="offset-4@md 6@md 12@sm" 
  class="start"
  on:click={startTimer}
  disabled={isRunning}
  >Start
  </button>
</div>

<style>
  h2 {
    margin: 0;
  }

  .start {
    background-color: #0072bb;
    width: 100%;
    margin: 10px 0;
  }

  .start[disabled] {
    background-color: rgb(194,194,194);
    color: #000;
    cursor: not-allowed;
  }
</style>