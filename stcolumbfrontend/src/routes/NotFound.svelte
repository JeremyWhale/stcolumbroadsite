<script>
    export let message = "Page not found";
</script>

<main>
    <h1>{message}</h1>
    <h2>404 :(</h2>
    <p>Sorry, the page you are looking for does not exist.</p>
</main>

<style>
    main {
        text-align: center;
        padding: 2rem;
    }

    h1 {
        font-size: 2rem;
        margin-bottom: 1rem;
    }

    p {
        font-size: 1.2rem;
    }
</style>