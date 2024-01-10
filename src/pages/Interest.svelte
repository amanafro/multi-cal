<script>
    let loan;
    let percentage;
    let period = 12;
    let result = 0;

    let selectedMonth = 4; // Initialize with a default value
    let months = [4, 6, 8, 10, 12, 16, 20, 24, 30, 36];

    function interestRateConverter() {
        result = loan * (percentage / 100) * (selectedMonth / period);
        // No need to use parseFloat here
        result = result.toFixed(2);
    }
</script>

<main>
    <label>
        <h3>calculate interest rate</h3>
        input in the amount of loan<br>
        <input type="number" bind:value={loan}><br>
        input in interest rate<br>
        <input type="number" bind:value={percentage}><br>
        select the period (month)<br>
        <select bind:value={selectedMonth}>
            {#each months as month}
                <option>{month}</option>
            {/each}
        </select><br>
        <button on:click={interestRateConverter}>calculate</button><br>
        <span>{"CHF " + result}</span>
    </label>
</main>