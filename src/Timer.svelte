<script>
  import ProgressBar from './ProgressBar.svelte';
</script>

<div bp="grid">
  <h2 bp="offset-5@md 4@md 12@sm">Seconds Left :</h2>
</div>

<ProgressBar />

<div bp="grid">
  <button class="start" bp="offset-5@md 4@md 12@sm">Start</button>
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
</style>