<script>
  import Home from './pages/Home.svelte'
  import Length from './pages/Length.svelte'
  import Temperature from './pages/Temperature.svelte'
  import Percentage from './pages/Percentage.svelte'
  import Interestrate from './pages/InterestRate.svelte'
  import Area from './pages/Area.svelte'
  import { Router, Route } from 'svelte-routing';
</script>

<Router>
    <Route path="/" component={Home}/>
    <Route path="/Length" component={Length}/>
    <Route path="/Temperature" component={Temperature}/>
    <Route path="/Area" component={Area}/>
    <Route path="/Percentage" component={Percentage}/>
    <Route path="/Interest rate" component={Interestrate}/>
</Router>