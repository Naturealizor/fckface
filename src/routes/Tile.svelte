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
