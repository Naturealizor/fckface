<script>
  // import tile
  import Tile from "./Tile.svelte";

  // create array of audio sources
  const tiles = [
    {
      audioSrc: "FckFace_Clips/FckfaceWall_Cut1.mp3",
      name: "first fart",
    },
    {
      audioSrc: "FckFace_Clips/FckfaceWall_Cut2.mp3",
      name: "freebirds",
    },
    {
      audioSrc: "FckFace_Clips/FckfaceWall_Cut3.mp3",
      name: "biology homework",
    },
    { audioSrc: "FckFace_Clips/FckfaceWall_Cut4.mp3", name: "SUV fart" },
    {
      audioSrc: "FckFace_Clips/FckfaceWall_Cut5.mp3",
      name: "baseball bats",
    },
    { audioSrc: "FckFace_Clips/clip (2).mp3", name: "my name is" },
    { audioSrc: "FckFace_Clips/clip (3).mp3", name: "final part" },
    { audioSrc: "FckFace_Clips/clip (4).mp3", name: "bomb pops" },
    {
      audioSrc: "FckFace_Clips/clip (5).mp3",
      name: "gassed himself out",
    },
    {
      audioSrc: "FckFace_Clips/clip (6).mp3",
      name: "taco bell drive through",
    },
    { audioSrc: "FckFace_Clips/clip (8).mp3", name: "*shrug*" },
    { audioSrc: "FckFace_Clips/clip (9).mp3", name: "relief" },
    { audioSrc: "FckFace_Clips/clip (11).mp3", name: "yeah!" },
    { audioSrc: "FckFace_Clips/clip (12).mp3", name: "am I ok?" },
    { audioSrc: "FckFace_Clips/clip (13).mp3", name: "???" },
    { audioSrc: "FckFace_Clips/clip (14).mp3", name: "what was that" },
    { audioSrc: "FckFace_Clips/clip (15).mp3", name: "we agreed" },
    { audioSrc: "FckFace_Clips/clip (17).mp3", name: "real name" },
    { audioSrc: "FckFace_Clips/clip (19).mp3", name: "eww eww" },
    {
      audioSrc: "FckFace_Clips/clip (20).mp3",
      name: "bought a porta potty",
    },
    {
      audioSrc: "FckFace_Clips/clip (23).mp3",
      name: "we got salad cream frozen",
    },
    {
      audioSrc: "FckFace_Clips/clip (24).mp3",
      name: "another root canal",
    },
    { audioSrc: "FckFace_Clips/clip (25).mp3", name: "geoff" },
    { audioSrc: "FckFace_Clips/clip (28).mp3", name: "it shot out" },
    {
      audioSrc: "FckFace_Clips/clip (29).mp3",
      name: "fucked up so bad",
    },
    {
      audioSrc: "FckFace_Clips/clip (31).mp3",
      name: "definition of condiment",
    },
    { audioSrc: "FckFace_Clips/clip (33).mp3", name: "iunno" },
    { audioSrc: "FckFace_Clips/clip (37).mp3", name: "???" },
    { audioSrc: "FckFace_Clips/clip (40).mp3", name: "my name is wtf" },
    { audioSrc: "FckFace_Clips/clip (42).mp3", name: "andrew gag" },
    { audioSrc: "FckFace_Clips/clip (43).mp3", name: "all the bov" },
    {
      audioSrc: "FckFace_Clips/clip (46).mp3",
      name: "sat in the little..",
    },
    { audioSrc: "FckFace_Clips/clip (47).mp3", name: "???" },
    { audioSrc: "FckFace_Clips/clip (48).mp3", name: "???" },
    {
      audioSrc: "FckFace_Clips/clip (49).mp3",
      name: "you look like dog shit",
    },
    { audioSrc: "FckFace_Clips/clip (50).mp3", name: "???" },
    { audioSrc: "FckFace_Clips/clip (55).mp3", name: "???" },
    { audioSrc: "FckFace_Clips/clip (58).mp3", name: "relief two" },
    { audioSrc: "FckFace_Clips/clip (61).mp3", name: "???" },
    { audioSrc: "FckFace_Clips/clip (62).mp3", name: "???" },
    { audioSrc: "FckFace_Clips/clip (67).mp3", name: "???" },
    {
      audioSrc: "FckFace_Clips/clip (69).mp3",
      name: "what's that noise",
    },
    { audioSrc: "FckFace_Clips/clip (72).mp3", name: "???" },
  ];

  // let isHover = true;

  // function switchToClick() {
  //   isHover = false;
  // }
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
