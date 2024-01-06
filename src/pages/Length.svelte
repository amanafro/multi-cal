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
    input in miles
    <input type="number" bind:value={miles1}>
    <button on:click={milesToKM}>Calculate</button>
    <p>{parseFloat(km1.toFixed(2)) + " km"}</p>
    </label>

</main>

<main>
    <label>
    <h3>{title}</h3>
    input in km
    <input type="number" bind:value={km2}>
    <button on:click={kmToMiles}>Calculate</button>
    <p>{parseFloat(miles2.toFixed(2)) + " miles"}</p>
    </label>
</main>

<style>

    main {
        display: grid;
        place-items: center;
        max-height: 100dvh;
        background-color: beige;
        padding: 3rem;
        border-radius: .75rem;
    }

    h3, p {
        color: black;
        font-size: 2rem;
    }

</style>