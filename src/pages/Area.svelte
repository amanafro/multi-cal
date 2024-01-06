<script>

    const title = "calculate area";

    let celsius1 = 0;
    let fahrenheit1 = 0;
    let conversion1 = 9/5;

    const PI = 3.141592;

    let side1 = 0;
    let side2 = 0;

    let squareArea = 0;

    function square() {
        squareArea = side1 * side2;
        return squareArea;

    }
    function triangle() {

    }
    function rectangle() {

    }
    function circle() {

    }


</script>

<main>
    <label>
        <h3>{title}</h3>
        input the first side
        <input type="number" bind:value={celsius1}>
        <input type="number" bind:value={celsius1}>
        <button on:click={}>Calculate</button>
        <p>{parseFloat(fahrenheit1.toFixed(2)) + " °F"}</p>
    </label>
</main>

<main>
    <label>
        <h3>{title}</h3>
        input in fahrenheit
        <input type="number" bind:value={}>
        <button on:click={}>Calculate</button>
        <p>{parseFloat(.toFixed(2)) + " °C"}</p>
    </label>
</main>

<main>
    <label>
        <h3>{title}</h3>
        input in fahrenheit
        <input type="number" bind:value={}>
        <button on:click={}>Calculate</button>
        <p>{parseFloat(.toFixed(2)) + " °C"}</p>
    </label>
</main>

<main>
    <label>
        <h3>{title}</h3>
        input in fahrenheit
        <input type="number" bind:value={}>
        <button on:click={}>Calculate</button>
        <p>{parseFloat(.toFixed(2)) + " °C"}</p>
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