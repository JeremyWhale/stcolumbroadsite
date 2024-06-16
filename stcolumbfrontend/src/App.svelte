<script lang="ts">
  import { Router, Route, Link } from 'svelte-routing';
  import Banner from './lib/Banner.svelte';
  import Navbar from './lib/Navbar.svelte';
  import Home from './routes/Home.svelte';
  import Where from './routes/Where.svelte';
  import Units from './routes/Units.svelte';
  import About from './routes/About.svelte';
</script>

<Router>
  <main>
    <Banner/>
    <Navbar/>
    <Route path="/" component={Home} />
    <Route path="/about" component={About} />
    <Route path="/where" component={Where} />
    <Route path="/units" component={Units} />
  </main>
</Router>

<style>
  main {
    width: 100%;
  }
</style>