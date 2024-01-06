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
    input in celsius<br>
    <input type="number" bind:value={celsius1}><br>
    <button on:click={celsiusToFahrenheit}>Calculate</button><br>
    <span>{parseFloat(fahrenheit1.toFixed(2)) + " °F"}</span>
    </label>
</main>


<main>
    <label>
    <h3>{title}</h3>
    input in fahrenheit<br>
    <input type="number" bind:value={fahrenheit2}><br>
    <button on:click={fahrenheitToCelsius}>Calculate</button><br>
    <span>{parseFloat(celsius2.toFixed(2)) + " °C"}</span>
    </label>
</main>



<style>
</style>