<script>
  import { onMount } from "svelte";

  export let audioSrc;
  export let name;
  let audio;
  let isAudioPlaying = false;

  onMount(() => {
    audio = new Audio(audioSrc);
  });

  function playAudio() {
    while (!isAudioPlaying) {
      audio.play();
      isAudioPlaying = true;
    }
  }
</script>

<div on:click={playAudio} on:keypress={playAudio}>
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
