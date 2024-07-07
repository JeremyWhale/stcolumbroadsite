<script lang="ts">
    import { Carousel } from 'flowbite-svelte';
    const images = [
        {
      alt: 'Image of Site St Columb Road Industrial Units for let',
      src: '/IMG_3534.jpg',
      title: 'Unit-1E-StColumbRoad-Industrial-Units-For-Rent'
    },
    {
      alt: 'Image of Site St Columb Road Industrial Units for let',
      src: '/IMG_3527.jpg',
      title: 'Unit-1E-StColumbRoad-Industrial-Units-For-Rent'
    },

    ];

</script>

<main>
    <div class ="container">
        <Carousel {images} class="max-w-4xl" imgClass="object-contain h-fit w-fit rounded-sm" let:Controls>
            <Controls />
        </Carousel>
    </div>
</main>

<style>
    .carousel img{
        width: 50%; /* Ensure the image fills the container width */
        height: auto;
        width: auto; /* Adjust height automatically to maintain aspect ratio */
        object-fit: contain; /* Ensure the full image is visible */
    }
    .container img {
    max-width: 50%;
    height: auto;
    }
</style>