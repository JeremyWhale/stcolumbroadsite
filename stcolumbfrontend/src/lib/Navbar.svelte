<script>
    import { Link } from "svelte-routing";

    let activeRoute = "";

    const routes = [
        { name: "Home", path: "/" },
        { name: "Units to Rent", path: "/units" },
        { name: "Find Us", path: "/where" },
        { name: "About", path: "/about" },
    ];
</script>

<nav>
    <div class="nav-links">
        <Link to={"/"} on:click={() => activeRoute = "/"}>
            <span><img src="/St_Columb_Road.png" alt="Home Icon" /></span>
        </Link>
        {#each routes as route}
            {#if route.name === "Home"}
                <Link
                to={route.path}
                on:click={() => activeRoute = route.path}
            >
                <span class:selected={activeRoute === route.path}>{route.name}</span>
            </Link>
            {:else}
                <Link
                to={route.path}
                on:click={() => activeRoute = route.path}
            >
                <span class:selected={activeRoute === route.path}>{route.name}</span>
            </Link>
            {/if}
        {/each}
    </div>
    <div class="contact-info">
        For enquiries
    </div>
    <div class="contact-info">
        Tel: 01726 73173 or 07733 534 438 | Email: whalecommercial@gmail.com
    </div>
</nav>

<style>
    nav {
        display: flex;
        position: sticky;
        flex-direction: column;
        justify-content: center;
        padding: 1rem;
        background-color: #cccccc;
        border-radius: 10px;
        top: 0;
        z-index: 1;
    }
    .nav-links {
        display: flex;
        justify-content: center;
    }

    a {
        display: flex;
        align-items: center;
        text-decoration: none;
        text-align: center;
        color: #333;
        padding: 0.5rem;
        align-items: center;
        justify-content: center;
        width: 100%;
        font-size: 1rem; /* adjust as needed */
        font-family: Arial, sans-serif; /* adjust as needed */
    }
    span {
        border-radius: 10px;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-right: 10px;
        height: 200px;
        width: 200px;
        background-color: rgb(255, 255, 255);
    }
    span img {
        border-radius: 10px; /* add this line */
    }
    span:hover {
        outline: 2px solid blue;
    }

    .selected {
        font-weight: bold;
    }

    .contact-info {
        display: block;
    }


    img {
        height: 200px; /* adjust as needed */
        width: 200px; /* adjust as needed */
    }
</style>