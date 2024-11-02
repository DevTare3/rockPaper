<script lang="ts">
  import pentagon from "$lib/images/bg-pentagon.svg";
  import rock from "$lib/images/icon-rock.svg";
  import paper from "$lib/images/icon-paper.svg";
  import scissors from "$lib/images/icon-scissors.svg";
  import spock from "$lib/images/icon-spock.svg";
  import lizard from "$lib/images/icon-lizard.svg";
  let score = $state("0");
  let moves = [
    { url: `${rock}`, name: "Rock" },
    { url: `${paper}`, name: "Paper" },
    { url: `${scissors}`, name: "Scissors" },
    { url: `${spock}`, name: "Spock" },
    { url: `${lizard}`, name: "Lizard" },
  ];
  import Game from "./components/mainGameComponent/game.svelte";
</script>

<header class="px-16 py-12">
  <div class="flex justify-between p-2 outline-1 outline">
    <h1 class="text-white text-xl">
      ROCK <br /> PAPER <br /> SCCISSORS <br /> LIZARD <br /> SPOCK
    </h1>
    <div>
      <p>SCORE</p>
      <p>{score}</p>
    </div>
  </div>
</header>
<main class="px-16 py-12">
  <div>
    <div>
      <img src={pentagon} alt="background layer of the game" />
    </div>
    {#each moves as move}
      <button><img src={move.url} alt={move.name} /></button>
    {/each}
  </div>
</main>
<footer class="px-16 py-12">
  <Game />
</footer>
<p>You Picked The House Picked You Win You Lose Play Again</p>
