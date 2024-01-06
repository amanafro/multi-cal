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
        input the first side<br>
        <input type="number" bind:value={side1}><br>
        input the second side<br>
        <input type="number" bind:value={side2}><br>
        <button on:click={square}>Calculate</button><br>
        <span>{parseFloat(squareArea.toFixed(2)) + " cm²"}</span>
    </label>
</main>

<main>
    <label>
        <h3>{title}</h3>
        input the first side<br>
        <input type="number" bind:value={side1}><br>
        input the second side<br>
        <input type="number" bind:value={side2}><br>
        <button on:click={triangle}>Calculate</button><br>
        <span>{parseFloat(triangleArea.toFixed(2)) + " cm²"}</span>
    </label>
</main>

<style>


</style>