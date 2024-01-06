<script>

    const title = "calculate area";

    let celsius1 = 0;
    let fahrenheit1 = 0;
    let conversion1 = 9/5;

    const PI = 3.141592;

    let side1 = 0;
    let side2 = 0;

    let squareArea = 0;
    let triangleArea = 0;
    let rectangleArea = 0;
    let circleArea = 0;

    let radius = 0;

    function square() {
        squareArea = side1 * side2;
        return squareArea;

    }
    function triangle() {
        triangleArea = (side1 * side2) * .5;
        return triangleArea;
    }
    function rectangle() {
        rectangleArea = side1 * side2;
    }
    function circle() {
        circleArea = PI * radius^2
        return circleArea;
    }


</script>
<main>
    <label>
        <h3>{title}</h3>
        input the first side
        <input type="number" bind:value={side1}>
        input the second side
        <input type="number" bind:value={side2}>
        <button on:click={square}>Calculate</button>
        <p>{parseFloat(squareArea.toFixed(2)) + " cm²"}</p>
    </label>
</main>

<main>
    <label>
        <h3>{title}</h3>
        input the first side
        <input type="number" bind:value={side1}>
        input the second side
        <input type="number" bind:value={side2}>
        <button on:click={triangle}>Calculate</button>
        <p>{parseFloat(triangleArea.toFixed(2)) + " cm²"}</p>
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