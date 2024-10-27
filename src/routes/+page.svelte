<script lang="ts">
    let score = $state('0');

    let moves = [
        {url:'../images/icon-lizard.svg' , name:'lizard'},
        {url:'../images/icon-rock.svg', name:'rock'},
        {url:'../images/icon-paper.svg', name:'paper'},
        {url:'../images/icon-scissors.svg', name:'scissors'},
        {url:'../images/icon-spock.svg', name:'spock'},
    ]
</script>
<main>
    <div>
        <img src="../images/icon-spock.svg" alt="aaa">
        <img src="../images/logo-bonus.svg" alt="The logo of the game!">
        <div>
            <p>SCORE</p>
            <p>{score}</p>
        </div>
    </div>
    
    <div>
        <div><img src="../images/bg-pentagon.svg" alt="background layer of the game"></div>
        {#each moves as move}
            <button><img src={move.url} alt={move.name}></button>
            {/each}
    </div>
</main>
<footer>
    <p>RULES</p>
</footer>
You Picked
The House Picked

You Win
You Lose

Play Again