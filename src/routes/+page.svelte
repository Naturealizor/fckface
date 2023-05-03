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
    { audioSrc: "src/FckFace Wall/FckfaceWall_Cut4.mp3", name: "tbd" },
    { audioSrc: "src/FckFace Wall/clip (1).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (2).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (3).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (4).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (5).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (6).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (7).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (8).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (9).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (10).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (11).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (12).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (13).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (14).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (15).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (16).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (17).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (18).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (19).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (20).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (21).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (22).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (23).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (24).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (25).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (26).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (27).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (28).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (29).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (30).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (31).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (32).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (33).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (34).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (35).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (36).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (37).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (38).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (39).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (40).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (41).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (42).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (43).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (44).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (45).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (46).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (47).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (48).mp3", name: "test" },
    { audioSrc: "src/FckFace Wall/clip (49).mp3", name: "test" },
  ];
</script>

<h1 class="centered-text">Welcome to the Wall of Best of F**kFace!</h1>
<p class="centered-text">
  Listen to the original here <a
    href="https://www.youtub@e.com/watch?v=_5v7MpXPfjk">here!</a
  > (Warning!! If you don't think fart jokes are funny, you may want to leave now)
</p>
<p class="centered-text">
  I really can't say why exactly I wanted to make this, other than I got bored
  and this popped into my head. I hope you enjoy it!
</p>

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
</style>
