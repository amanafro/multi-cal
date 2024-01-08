<script>

    let loan;
    let percentage;
    let period = 12;
    let result = 0;

    let selectedMonth;
    let months = [4, 6, 8, 10, 12, 16, 20, 24, 30, 36];


    function interestRateConverter() {
        result = loan * (percentage / 100) * (selectedMonth / period);
        return result;
    }

    </script>

<main>
    <label>
        <h3>calculate interest rate</h3>
        input in the amount of loan<br>
        <input type="number" bind:value={loan}><br>
        input in interest rate<br>
        <input type="number" bind:value={percentage}><br>
        input in interest rate<br>
        <select bind:value={selectedMonth}>
        {#each months as month}
            <option>{month}</option>
        {/each}
        </select>
        {#if selectedMonth}
            <p>selected {selectedMonth}</p>
        {/if}
        <button on:click={interestRateConverter}>Calculate</button><br>
        <span>{"CHF "+parseFloat(result.toFixed(2))}</span>
    </label>
</main>
