<script>
  // import tile
  import Tile from "./Tile.svelte";

  // create array of audio sources
  const tiles = [
    { audioSrc: "src/FckFace Wall/FckfaceWall_Cut1.mp3" },
    { audioSrc: "src/FckFace Wall/FckfaceWall_Cut2.mp3" },
    { audioSrc: "src/FckFace Wall/FckfaceWall_Cut3.mp3" },
    { audioSrc: "src/FckFace Wall/FckfaceWall_Cut4.mp3" },
  ];

  let titles = [
    { id: "Cut 1", name: "first fart" },
    { id: "Cut 2", name: "freebirds" },
    { id: "Cut 3", name: "biology homework" },
  ];
</script>

<h1 class="centered-text">Welcome to the Wall of Best of Fu*kFace!</h1>
<p class="centered-text">
  Listen to the original here <a
    href="https://www.youtube.com/watch?v=_5v7MpXPfjk">here!</a
  > (Warning!! If you don't think fart jokes are funny, you may want to leave now)
</p>
<p class="centered-text">
  I really can't say why exactly I wanted to make this, other than I got bored
  and this popped into my head. I hope you enjoy it!
</p>

<div class="container">
  {#each tiles as tile, i}
    <div class="card">
      <Tile audioSrc={tile.audioSrc} title={titles[i]} />
      <!-- {titles.forEach(function (titles) {
        console.log(titles); -->
      <!-- })} -->
      <!-- {#each titles as title, i}
        <div class="title">
          {i + 1}:
          <p>{title.id}: {title.name}</p>
        </div>
      {/each} -->
    </div>
  {/each}
</div>

<style>
  /* //create centered text class */
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
</style>
