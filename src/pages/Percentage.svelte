<script>
    let amount ;
    let percentage;
    let result = 0;

    function percentageCalculator() {
        result = amount * percentage / 100;
        result = result.toFixed(2);
        return result;
    }
</script>

<main>
<label>

    <h3>calculate percentage</h3>
    input the percentage<br>
    <input type="number" bind:value={percentage}><br>
    input the amount<br>
    <input type="number" bind:value={amount}><br>
    <button on:click={percentageCalculator}>Calculate</button><br>
    <span>{result + " amount"}</span>
</label>
</main>
