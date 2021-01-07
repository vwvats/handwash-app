<script>
  import Timer from './Timer.svelte';
  import HowTo from './HowTo.svelte';
  let audio;
  function timerEnd(e) {
    audio.play();
  }
</script>

<h1>Handwashing App</h1>
<Timer on:end={timerEnd}/>
<HowTo />
<audio bind:this={audio}>
  <source src="end-sound.wav">
  <track default
    kind="captions"
    srclang="en"
    src="">
</audio>

<style>
  h1 {
    color: #0072bb;
    text-align: center;
  }
</style>
