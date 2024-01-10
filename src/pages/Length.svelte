<script>

    const title = "calculate length";

    let miles1 = 0;
    let km1 = 0;
    const conversionMiles = 1.60934;

    function milesToKM() {
        km1 = miles1 * conversionMiles
        km1 = km1.toFixed(2);
        return km1;
    }

    let miles2 = 0;
    let km2 = 0;
    const conversionKM = 0.62137;
    function kmToMiles() {
        miles2 = km2 * conversionKM
        miles2 = miles2.toFixed(2);
        return miles2;
    }

    import Switch from "../components/Switch.svelte";

    let switchChoice = false;

</script>
<div>
    {#if switchChoice === false}
        <main>
            <label>
                <h3>{title}</h3>
                input in miles<br>
                <input type="number" bind:value={miles1}><br>
                <button on:click={milesToKM}>Calculate</button><br>
                <span>{km1 + " KM"}</span>
            </label>
            <div class="switch">
                <span>KM</span>
                <Switch bind:checked={switchChoice}></Switch><br>
                <span>M</span>
            </div>
        </main>
    {/if}


    {#if switchChoice === true}
        <main>
            <label>
                <h3>{title}</h3>
                input in km<br>
                <input type="number" bind:value={km2}><br>
                <button on:click={kmToMiles}>Calculate</button><br>
                <span>{miles2+ " Miles"}</span>
            </label>
            <div class="switch">
                <span>KM</span>
                <Switch bind:checked={switchChoice}></Switch><br>
                <span>M</span>
            </div>
        </main>
    {/if}
</div>