<script>

    let celsius2 = 0;
    let fahrenheit2;
    let conversion2 = 5/9;

    function fahrenheitToCelsius() {
        celsius2 = conversion2 * (fahrenheit2 - 32);
        celsius2 = celsius2.toFixed(2);
        return celsius2;
    }

    const title = "calculate temperature";

    let celsius1;
    let fahrenheit1 = 0;
    let conversion1 = 9/5;

    function celsiusToFahrenheit() {
        fahrenheit1 = (conversion1 * celsius1) + 32;
        fahrenheit1 = fahrenheit1.toFixed(2);
        return fahrenheit1;
    }

    import Switch from "../components/Switch.svelte";

    let switchChoice = false;

</script>

<div>

    {#if switchChoice === false}
        <main>
            <label>
                <h3>{title}</h3>
                input in fahrenheit<br>
                <input type="number" bind:value={fahrenheit2}><br>
                <button on:click={fahrenheitToCelsius}>Calculate</button><br>
                <span>{parseFloat(celsius2) + " °C"}</span>
            </label>
            <div class="switch">
                <span>°C</span>
                <Switch bind:checked={switchChoice}></Switch><br>
                <span>°F</span>
            </div>
        </main>
        {/if}
    {#if switchChoice === true}
        <main>
            <label>
                <h3>{title}</h3>
                input in celsius<br>
                <input type="number" bind:value={celsius1}><br>
                <button on:click={celsiusToFahrenheit}>Calculate</button><br>
                <span>{parseFloat(fahrenheit1.toFixed(2)) + " °F"}</span>
            </label>
            <div class="switch">
                <span>°C</span>
                <Switch bind:checked={switchChoice}></Switch><br>
                <span>°F</span>
            </div>
        </main>
        {/if}

</div>

<style>
    .switch {
        padding: 1rem 0;
    }
</style>


