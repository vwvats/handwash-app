<script>
  import Timer from './Timer.svelte';
  import HowTo from './HowTo.svelte';
</script>

<h1>Handwashing App</h1>
<Timer />
<HowTo />
<audio>
  <source src="end-sound.wav">
</audio>

<style>
  h1 {
    color: #0072bb;
    text-align: center;
  }
</style>
