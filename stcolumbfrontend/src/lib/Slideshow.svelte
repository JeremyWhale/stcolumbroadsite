<script lang="ts">
    let images = [
        '/IMG_3522.jpg',
        '/IMG_3523.jpg',
        '/IMG_3524.jpg',
        '/IMG_3526.jpg',
        '/IMG_3527.jpg',
        '/IMG_3528.jpg',
        '/IMG_3529.jpg',
        '/IMG_3530.jpg',
        '/IMG_3531.jpg',
        '/IMG_3532.jpg',
        '/IMG_3533.jpg',
    ];

    let currentIndex = 0;

    function nextSlide() {
        currentIndex = (currentIndex + 1) % images.length;
    }

    setInterval(nextSlide, 5000); // Change image every 5 seconds
</script>

<main>
    {#if images.length > 0}
        <img src={images[currentIndex]} alt="Slideshow Image" class="fade" />
    {:else}
        <p>No images found.</p>
    {/if}
</main>

<style>
    main {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 10px;
    }

    img {
        max-width: 100%;
        height: auto;
        margin-bottom: 1rem;
    }

    .fade {
        animation: fade 5s infinite;
    }

    @keyframes fade {
        0%, 100% { opacity: 0; }
        50% { opacity: 1; }
    }
</style>