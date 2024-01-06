<script>
  import Home from './pages/Home.svelte'
  import Length from './pages/Length.svelte'
  import Temperature from './pages/Temperature.svelte'
  import Speed from './pages/Speed.svelte'
  import Area from './pages/Area.svelte'
  import { Router, Route } from 'svelte-routing';
</script>

<Router>
    <Route path="/" component={Home}/>
    <Route path="/Length" component={Length}/>
    <Route path="/Temperature" component={Temperature}/>
    <Route path="/Speed" component={Speed}/>
    <Route path="/Area" component={Area}/>
</Router>

<main>

</main>

<style>

</style>
