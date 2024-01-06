<script>

    const title = "calculate temperature";

    let celsius1 = 0;
    let fahrenheit1 = 0;
    let conversion1 = 9/5;

    function celsiusToFahrenheit() {
        fahrenheit1 = conversion1 * (celsius1 + 32);
        return fahrenheit1;
    }

    let celsius2 = 0;
    let fahrenheit2 = 0;
    let conversion2 = 5/9;

    function fahrenheitToCelsius() {
        celsius2 = conversion2 * (fahrenheit2 - 32);
        return celsius2;
    }

</script>


<main>
    <label>
    <h3>{title}</h3>
    input in celsius
    <input type="number" bind:value={celsius1}>
    <button on:click={celsiusToFahrenheit}>Calculate</button>
    <p>{parseFloat(fahrenheit1.toFixed(2)) + " °F"}</p>
    </label>
</main>


<main>
    <label>
    <h3>{title}</h3>
    input in fahrenheit
    <input type="number" bind:value={fahrenheit2}>
    <button on:click={fahrenheitToCelsius}>Calculate</button>
    <p>{parseFloat(celsius2.toFixed(2)) + " °C"}</p>
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