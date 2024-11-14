<script lang="ts">
  import pentagon from "$lib/images/bg-pentagon.svg";
  import rock from "$lib/images/icon-rock.svg";
  import paper from "$lib/images/icon-paper.svg";
  import scissors from "$lib/images/icon-scissors.svg";
  import spock from "$lib/images/icon-spock.svg";
  import lizard from "$lib/images/icon-lizard.svg";
  import logo from "$lib/images/logo-bonus.svg";
  let score = $state("12");
  let moves = [
    {
      url: `${rock}`,
      name: "Rock",
      gradient:
        "bg-gradient-to-b from-rock-gradient-start to-rock-gradient-end",
      position: "bottom-10 right-5",
    },
    {
      url: `${paper}`,
      name: "Paper",
      gradient:
        "bg-gradient-to-b from-paper-gradient-start to-paper-gradient-end",
      position: "top-5 right-5",
    },
    {
      url: `${scissors}`,
      name: "Scissors",
      gradient:
        "bg-gradient-to-b from-scissors-gradient-start to-scissors-gradient-end",
      position: "top-10",
    },
    {
      url: `${spock}`,
      name: "Spock",
      gradient:
        "bg-gradient-to-b from-spock-gradient-start to-spock-gradient-end",
      position: "left-10",
    },
    {
      url: `${lizard}`,
      name: "Lizard",
      gradient:
        "bg-gradient-to-b from-lizard-gradient-start to-lizard-gradient-end",
      position: "left-5 bottom-5",
    },
  ];
  import Rules from "./components/rulesComponent/rules.svelte";
</script>

<header class="px-12 py-8">
  <div
    class="flex justify-between items-center p-4 outline-4 outline outline-header-outline rounded-sm"
  >
    <div class="w-16"><img src={logo} alt="logo of the game" /></div>
    <div class="bg-white py-2 px-6 rounded-md text-center">
      <p class="text-score-text font-bold text-base tracking-widest">SCORE</p>
      <p class="text-5xl font-bold text-dk-text">{score}</p>
    </div>
  </div>
</header>
<main class="px-12 py-8">
  <div>
    <div>
      <img
        class="relative top-4"
        src={pentagon}
        alt="background layer of the game"
      />
    </div>
    {#each moves as move}
      <div class=" {move.gradient} rounded-full p-3 w-fit absolute">
        <button class="bg-white rounded-full p-5 size-20"
          ><img class="size-11/12" src={move.url} alt={move.name} /></button
        >
      </div>
    {/each}
  </div>
</main>
<footer class="px-16 py-12">
  <Rules />
</footer>
<p>You Picked The House Picked You Win You Lose Play Again</p>
