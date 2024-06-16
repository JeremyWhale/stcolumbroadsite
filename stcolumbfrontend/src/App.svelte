<script lang="ts">
  import { Router, Route, Link } from 'svelte-routing';
  import Banner from './lib/Banner.svelte';
  import Navbar from './lib/Navbar.svelte';
  import Home from './routes/Home.svelte';
  import About from './routes/About.svelte';
</script>

<Router>
  <main>
    <Navbar/>
    <Banner/>
    <Route path="/" component={Home} />
    <Route path="/about" component={About} />
  </main>
</Router>

<style>
  main {
    width: 100%;
  }
</style>