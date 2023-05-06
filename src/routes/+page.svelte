<script>
  // import tile
  import Tile from "./Tile.svelte";

  // create array of audio sources
  const tiles = [
    { audioSrc: "src/FckFace Wall/FckfaceWall_Cut1.mp3", name: "first fart" },
    { audioSrc: "src/FckFace Wall/FckfaceWall_Cut2.mp3", name: "freebirds" },
    {
      audioSrc: "src/FckFace Wall/FckfaceWall_Cut3.mp3",
      name: "biology homework",
    },
    { audioSrc: "src/FckFace Wall/FckfaceWall_Cut4.mp3", name: "SUV fart" },
    {
      audioSrc: "src/FckFace Wall/FckfaceWall_Cut5.mp3",
      name: "baseball bats",
    },
    { audioSrc: "src/FckFace Wall/clip (2).mp3", name: "my name is" },
    { audioSrc: "src/FckFace Wall/clip (3).mp3", name: "final part" },
    { audioSrc: "src/FckFace Wall/clip (4).mp3", name: "bomb pops" },
    { audioSrc: "src/FckFace Wall/clip (5).mp3", name: "gassed himself out" },
    {
      audioSrc: "src/FckFace Wall/clip (6).mp3",
      name: "taco bell drive through",
    },
    { audioSrc: "src/FckFace Wall/clip (8).mp3", name: "*shrug*" },
    { audioSrc: "src/FckFace Wall/clip (9).mp3", name: "relief" },
    { audioSrc: "src/FckFace Wall/clip (11).mp3", name: "yeah!" },
    { audioSrc: "src/FckFace Wall/clip (12).mp3", name: "am I ok?" },
    { audioSrc: "src/FckFace Wall/clip (13).mp3", name: "???" },
    { audioSrc: "src/FckFace Wall/clip (14).mp3", name: "what was that" },
    { audioSrc: "src/FckFace Wall/clip (15).mp3", name: "we agreed" },
    { audioSrc: "src/FckFace Wall/clip (17).mp3", name: "real name" },
    { audioSrc: "src/FckFace Wall/clip (19).mp3", name: "eww eww" },
    {
      audioSrc: "src/FckFace Wall/clip (20).mp3",
      name: "bought a porta potty",
    },
    {
      audioSrc: "src/FckFace Wall/clip (23).mp3",
      name: "we got salad cream frozen",
    },
    { audioSrc: "src/FckFace Wall/clip (24).mp3", name: "another root canal" },
    { audioSrc: "src/FckFace Wall/clip (25).mp3", name: "geoff" },
    { audioSrc: "src/FckFace Wall/clip (28).mp3", name: "it shot out" },
    { audioSrc: "src/FckFace Wall/clip (29).mp3", name: "fucked up so bad" },
    {
      audioSrc: "src/FckFace Wall/clip (31).mp3",
      name: "definition of condiment",
    },
    { audioSrc: "src/FckFace Wall/clip (33).mp3", name: "iunno" },
    { audioSrc: "src/FckFace Wall/clip (37).mp3", name: "???" },
    { audioSrc: "src/FckFace Wall/clip (40).mp3", name: "my name is wtf" },
    { audioSrc: "src/FckFace Wall/clip (42).mp3", name: "andrew gag" },
    { audioSrc: "src/FckFace Wall/clip (43).mp3", name: "all the bov" },
    { audioSrc: "src/FckFace Wall/clip (46).mp3", name: "sat in the little.." },
    { audioSrc: "src/FckFace Wall/clip (47).mp3", name: "???" },
    { audioSrc: "src/FckFace Wall/clip (48).mp3", name: "???" },
    {
      audioSrc: "src/FckFace Wall/clip (49).mp3",
      name: "you look like dog shit",
    },
    { audioSrc: "src/FckFace Wall/clip (50).mp3", name: "???" },
    { audioSrc: "src/FckFace Wall/clip (55).mp3", name: "???" },
    { audioSrc: "src/FckFace Wall/clip (58).mp3", name: "relief two" },
    { audioSrc: "src/FckFace Wall/clip (61).mp3", name: "???" },
    { audioSrc: "src/FckFace Wall/clip (62).mp3", name: "???" },
    { audioSrc: "src/FckFace Wall/clip (67).mp3", name: "???" },
    { audioSrc: "src/FckFace Wall/clip (69).mp3", name: "what's that noise" },
    { audioSrc: "src/FckFace Wall/clip (72).mp3", name: "???" },
  ];

  let isHover = true;

  function switchToClick() {
    isHover = false;
  }
</script>

<h1 class="centered-text">Welcome to the Wall of Best of F**kFace!</h1>
<p class="centered-text">
  Listen to the original here <a
    href="https://www.youtub@e.com/watch?v=_5v7MpXPfjk">here!</a
  > <br />(If you don't think fart jokes are funny, you may want to leave now)
</p>
<p class="centered-text">
  I really can't say why exactly I made this, other than I got bored and this
  popped into my head. I hope you enjoy it!
</p>
<p class="warning">
  headphone users and anyone in public warning!!!! <br />some of these clips are
  loud!!!<br />you might want to turn your volume down
</p>

<!-- <button on:click={switchToClick()}>Switch</button> -->

<div class="container">
  {#each tiles as tile}
    <div class="card">
      <Tile audioSrc={tile.audioSrc} name={tile.name} />
    </div>
  {/each}
</div>

<style>
  .centered-text {
    text-align: center;
  }
  p {
    font-size: 1.5rem;
  }
  .container {
    padding-top: 5%;
    margin: auto;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    justify-items: center;
    align-items: center;
    gap: 1rem;
    width: 50%;
  }
  .card {
    width: 50%;
    height: 50%;
    background-color: #f5f5f5;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 1rem;
    gap: 2rem;
  }
  .card:hover {
    cursor: pointer;
    background-color: #e5e5e5;
  }
  .warning {
    font-size: 2rem;
    color: red;
    text-align: center;
    text-transform: uppercase;
  }
</style>
