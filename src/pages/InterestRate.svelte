<script>

    let loan = 0;
    let percentage = 0;
    let period;
    let result;

    const months = [
        4,
        6,
        8,
        10,
        12,
        16,
        20,
        24,
        30,
        36
    ]


    function interestRateConverter() {
        result = loan * percentage * 100;
    }

</script>

<main>
    <label>
        <h3></h3>
        input in the amount of loan<br>
        <input type="number" bind:value={loan}><br>
        input in interest rate<br>
        <input type="number" bind:value={percentage}><br>
        input in interest rate<br>
        <select>
        {#each months as month}
            <option>{month}</option>
        {/each}
        </select>
        <button on:click={interestRateConverter}>Calculate</button><br>
        <span>{parseFloat("CHF " + result.toFixed(2))}</span>
    </label>
</main>

<style></style>