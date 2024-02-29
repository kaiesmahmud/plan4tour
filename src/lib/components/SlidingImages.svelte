<script lang="ts">
    import { Splide, SplideSlide } from '@splidejs/svelte-splide';
    import { onMount } from 'svelte';
    // Default theme
    import '@splidejs/svelte-splide/css';

    // or other themes
    import '@splidejs/svelte-splide/css/skyblue';
    // import '@splidejs/svelte-splide/css/sea-green';

    // or only core styles
    import '@splidejs/svelte-splide/css/core';
  
    let main: Splide;
    let thumbs: SplideSlide;
  
    const slides = [
        {
            src: 'https://images.unsplash.com/photo-1564501049412-61c2a3083791?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTZ8fGhvdGVsfGVufDB8fDB8fHww',
            alt: "some dummy data"
        },
        {
            src: 'https://images.unsplash.com/photo-1445991842772-097fea258e7b?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjB8fGhvdGVsfGVufDB8fDB8fHww',
            alt: "some dummy data"
        },
        {
            src: 'https://images.unsplash.com/photo-1611892440504-42a792e24d32?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MjJ8fGhvdGVsfGVufDB8fDB8fHww',
            alt: "some dummy data"
        },
        {
            src: 'https://images.unsplash.com/photo-1520250497591-112f2f40a3f4?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mjh8fGhvdGVsfGVufDB8fDB8fHww',
            alt: "some dummy data"
        },
    ]
  
    const mainOptions = {
      type      : 'loop',
      perPage   : 1,
      perMove   : 1,
      gap       : '1rem',
      pagination: false,
    //   height    : '10rem',
    };
  
    const thumbsOptions = {
      type        : 'slide',
      rewind      : true,
      gap         : '1rem',
      pagination  : false,
      arrows       :false,
      fixedWidth  : 110,
      fixedHeight : 70,
      cover       : true,
    //   focus       : 'center' as const,
      isNavigation: true,
      updateOnMove: true,
    };
  
    onMount( () => {
      if ( main && thumbs ) {
        main.sync( thumbs.splide );
      }
    } );
  </script>
  
  <div class=" w-1/2 flex flex-col">
    
    <Splide options={ mainOptions } bind:this={ main } aria-labelledby="thumbnails-example-heading">
      { #each slides as slide }
        <SplideSlide class="flex items-center justify-center">
          <img class="w-full rounded-lg" src={ slide.src } alt={ slide.alt }>
        </SplideSlide>
      { /each }
    </Splide>
  
    <Splide options={ thumbsOptions } bind:this={ thumbs }>
      { #each slides as slide }
        <SplideSlide>
          <img src={ slide.src } alt={ slide.alt }>
        </SplideSlide>
      { /each }
    </Splide>
  </div>