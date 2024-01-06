<script>

    const title = "calculate length";

    let miles1 = 0;
    let km1 = 0;
    const conversionMiles = 1.60934;

    function milesToKM() {
        km1 = miles1 * conversionMiles
        return km1;
    }

    let miles2 = 0;
    let km2 = 0;
    const conversionKM = 0.62137;
    function kmToMiles() {
        miles2 = km2 * conversionKM
        return miles2;
    }

</script>


<main>
    <label>
    <h3>{title}</h3>
    input in miles<br>
    <input type="number" bind:value={miles1}><br>
    <button on:click={milesToKM}>Calculate</button><br>
    <span>{parseFloat(km1.toFixed(2)) + " km"}</span>
    </label>

</main>

<main>
    <label>
    <h3>{title}</h3>
    input in km<br>
    <input type="number" bind:value={km2}><br>
    <button on:click={kmToMiles}>Calculate</button><br>
    <span>{parseFloat(miles2.toFixed(2)) + " miles"}</span>
    </label>
</main>

<style>



</style>