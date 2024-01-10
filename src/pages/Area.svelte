<script>

    const title = "calculate area";

    let selectedChoice;
    let choices = ["Square", "Triangle", "Rectangle", "Circle"];

    const PI = 3.141592;
    let radius;

    let side1;
    let side2;

    let squareArea = 0;
    let triangleArea = 0;
    let rectangleArea = 0;
    let circleArea = 0;

    function square() {
        squareArea = side1 * side1;
        triangleArea = squareArea.toFixed(2);
        return triangleArea;

    }
    function triangle() {
        triangleArea = (side1 * side2) * .5;
        triangleArea = triangleArea.toFixed(2);
        return triangleArea;
    }
    function rectangle() {
        rectangleArea = side1 * side2;
        rectangleArea = rectangleArea.toFixed(2);
        return rectangleArea;
    }
    function circle() {
        circleArea = PI * radius * radius;
        circleArea = circleArea.toFixed(2);
        return circleArea;
    }

</script>
<div>
    {#if selectedChoice === "Square"}
        <main>
            <label>
                <h3>{title}</h3>
                input the side<br>
                <input type="number" bind:value={side1}><br>
                <button on:click={square}>Calculate</button><br>
                <span>{parseFloat(squareArea.toFixed(2)) + " cm²"}</span>
            </label>
        </main>
        {/if}

    {#if selectedChoice === "Rectangle"}
        <main>
            <label>
                <h3>{title}</h3>
                input the height<br>
                <input type="number" bind:value={side1}><br>
                input the width<br>
                <input type="number" bind:value={side2}><br>
                <button on:click={rectangle}>Calculate</button><br>
                <span>{rectangleArea + " cm²"}</span>
            </label>
        </main>
        {/if}

    {#if selectedChoice === "Triangle"}
        <main>
            <label>
                <h3>{title}</h3>
                input the height<br>
                <input type="number" bind:value={side1}><br>
                input the base <br>
                <input type="number" bind:value={side2}><br>
                <button on:click={triangle}>Calculate</button><br>
                <span>{triangleArea + " cm²"}</span>
            </label>
        </main>
        {/if}

    {#if selectedChoice === "Circle"}
        <main>
            <label>
                <h3>{title}</h3>
                input the radius<br>
                <input type="number" bind:value={radius}><br>
                <button on:click={circle}>Calculate</button><br>
                <span>{circleArea + " cm²"}</span>
            </label>
        </main>
        {/if}

    <main>
        <label>
            choose an option
            <select bind:value={selectedChoice}>
                <option value="">Choose something</option>
                {#each choices as choice}
                    <option>{choice}</option>
                {/each}
            </select>
        </label>
    </main>
</div>