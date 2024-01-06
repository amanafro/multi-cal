<script>
    import LengthSvg from "../assets/LengthSvg.svg";
    import TemperatureSvg from "../assets/TemperatureSvg.svg";
    import AreaSvg from "../assets/area.svg";
    import SpeedSvg from "../assets/speed.svg";
    import { Link } from 'svelte-routing';
</script>

<main>
    <h2>welcome to multi-cal</h2>
    <div class="intro">
    <Link to="/Length"><img src={LengthSvg} alt="Length"/></Link>
    <Link to="/Temperature"><img src={TemperatureSvg} alt="Temperature" /></Link>
    <Link to="/Speed"><img src={SpeedSvg} alt="Area" /></Link>
    <Link to="/Area"><img src={AreaSvg} alt="Speed" /></Link>
    </div>
</main>

<style>
    .intro {
        display: flex;
        flex-direction: row;
        gap: 1rem;
    }

    @media only screen and (max-width: 600px) {
        main  {
            padding: 1rem;
        }
    }

</style>