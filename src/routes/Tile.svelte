<script>
  import { onMount } from "svelte";

  export let audioSrc;
  export let name;
  let audio;

  onMount(() => {
    audio = new Audio(audioSrc);
  });

  function playAudio() {
    audio.play();
    // add audio pause when playing the same clip again
    if (audio.paused) {
      audio.pause();
    }
  }

  // function to stop audio
  function stopAudio() {
    audio.pause();
  }
</script>

<!-- create a div to playAudio on hover -->
<!-- <div on:click={playAudio} on:keypress={playAudio}> -->
<div
  on:hover={playAudio}
  on:focus={playAudio}
  on:click={playAudio}
  on:keypress={playAudio}
>
  <div class="tile">
    <p>{name}</p>
  </div>
</div>

<style>
  .tile {
    text-align: center;
    cursor: pointer;
  }
</style>
