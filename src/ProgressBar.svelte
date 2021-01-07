<script>
  export let progress = 0;
</script>

<div bp="grid">
  <div bp="12@md 12@sm" class="progress-container">
    <div class="progress-bar" style="width: {progress}%;">
      <span class="sr-only">{progress}%</span>
    </div>
  </div>
</div>

<style>
  .progress-container {
    border: solid 2px rgb(194,194,194);
    margin: 10px 0;
  }

  .progress-bar {
    background-color: rgb(77,195,55);
    height: 30px;
  }
</style>