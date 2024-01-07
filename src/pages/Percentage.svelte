<script>
    let amount = 0;
    let percentage = 0;
    let result = 0;

    function percentageCalculator() {
        result = amount * percentage / 100;
        return result;
    }
</script>

<main>
<label>
    <h3>calculate percentage</h3>
    input the amount<br>
    <input type="number" bind:value={amount}><br>
    input the percentage<br>
    <input type="number" bind:value={percentage}><br>
    <button on:click={percentageCalculator}>Calculate</button><br>
    <span>{parseFloat(result.toFixed(2))}</span>
</label>
</main>
