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

<div on:mouseover={playAudio} on:focus={playAudio}>
  <div class="tile">
    <p>{name}</p>
  </div>
</div>
