<script lang="ts">
  import { Router, Route, Link } from 'svelte-routing';
  import Banner from './lib/Banner.svelte';
  import Navbar from './lib/Navbar.svelte';
  import Home from './routes/Home.svelte';
  import About from './routes/About.svelte';
  import Where from './routes/Where.svelte';
</script>

<Router>
  <main>
    <Banner/>
    <Navbar/>
    <Route path="/" component={Home} />
    <Route path="/about" component={About} />
    <Route path="/where" component={Where} />
  </main>
</Router>

<style>
  main {
    width: 100%;
  }
</style>