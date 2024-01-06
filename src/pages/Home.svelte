<script>
    import LengthSvg from "../assets/LengthSvg.svg";
    import TemperatureSvg from "../assets/TemperatureSvg.svg";
    import AreaSvg from "../assets/area.svg";
    import SpeedSvg from "../assets/speed.svg";
    import { Link } from 'svelte-routing';
</script>

<main>
    <Link to="/Length"><img src={LengthSvg} alt="Length"/></Link>
    <Link to="/Temperature"><img src={TemperatureSvg} alt="Temperature" /></Link>
    <Link to="/Speed"><img src={SpeedSvg} alt="Area" /></Link>
    <Link to="Area"><img src={AreaSvg} alt="Speed" /></Link>
</main>

<style>
    main {
        @apply grid place-item-center border-4 p-5 rounded-3xl gap-5 shadow-2xl;
    }
</style>