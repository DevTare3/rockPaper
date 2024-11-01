<script lang="ts">
  import pentagon from "$lib/images/bg-pentagon.svg";
  import rock from "$lib/images/icon-rock.svg";
  import paper from "$lib/images/icon-paper.svg";
  import scissors from "$lib/images/icon-scissors.svg";
  import spock from "$lib/images/icon-spock.svg";
  import lizard from "$lib/images/icon-lizard.svg";
  import * as AlertDialog from "$lib/components/ui/alert-dialog/index.js";
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

<main>
  <div>
    <img src={pentagon} alt="background layer of the game" />
    <div>
      <p>SCORE</p>
      <p>{score}</p>
    </div>
  </div>
  <AlertDialog.Root>
    <AlertDialog.Trigger>Show Dialog</AlertDialog.Trigger>
    <AlertDialog.Content>
      <AlertDialog.Header>
        <AlertDialog.Title>Are you absolutely sure?</AlertDialog.Title>
        <AlertDialog.Description>
          This action cannot be undone. This will permanently delete your
          account and remove your data from our servers.
        </AlertDialog.Description>
      </AlertDialog.Header>
      <AlertDialog.Footer>
        <AlertDialog.Cancel>Cancel</AlertDialog.Cancel>
        <AlertDialog.Action>Continue</AlertDialog.Action>
      </AlertDialog.Footer>
    </AlertDialog.Content>
  </AlertDialog.Root>

  <div>
    <div>
      <img src="../images/bg-pentagon.svg" alt="background layer of the game" />
    </div>
    {#each moves as move}
      <button><img src={move.url} alt={move.name} /></button>
    {/each}
  </div>
</main>
<footer>
  <p>RULES</p>
</footer>
<p>You Picked The House Picked You Win You Lose Play Again</p>
