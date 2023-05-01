<script>
  import { onMount } from "svelte";

  export let audioSrc;
  let audio;

  // let count = 0;
  // let newCount = (count += 1);
  // let titleStart = "Cut ";

  // let title = titleStart + newCount;
  // console.log(title);

  const titles = [
    { name: "first fart" },
    { name: "freebirds" },
    { name: "biology homework" },
  ];

  onMount(() => {
    audio = new Audio(audioSrc);
  });

  function playAudio() {
    audio.play();
  }

  function showTitle() {
    const tileElements = [];

    for (let i = 0; i < titles.length; i++) {
      const title = titles[i];
      tileElements.push({ title });
    }
    console.log(tileElements);
    return tileElements;
  }
</script>

<div on:mouseover={playAudio} on:focus={playAudio}>
  {#each titles as title, i}
    <div class="tile">
      <p>{title.forEach(title)}</p>
    </div>
  {/each}
</div>
