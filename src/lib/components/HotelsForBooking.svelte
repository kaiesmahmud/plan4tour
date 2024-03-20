<script>
    import { Splide, SplideSlide } from '@splidejs/svelte-splide';
    // Default theme
    import '@splidejs/svelte-splide/css';
    
    import { hotels } from './../constants/hotels'
  
    
</script>
<div class="flex flex-col items-center justify-center p-5"> 
    <section class="w-full lg:w-[80%] ">
        <div>
            <h2 class="text-2xl md:text-3xl lg:text-4xl py-5 md:p-5 font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-sky-700 to-cyan-400">Hotels for Booking</h2>
        </div>
        <div class="md:p-5">
            <Splide options={ {
                // type   : 'loop',
                // rewind: true,
                gap   : '1rem',
                autoplay:true,
                interval: 3000, // Set the duration to 1000ms (1 second)
                // autoWidth:true,
                // wheel    : true,
                perPage: 4,
                pagination:false,
                drag   : 'free',
                focus  : 'start',
                autoScroll: {
                  speed: 1,
                },
                breakpoints: {
                    640:{ 
                        arrows:false,
                        autoWidth:true,
                    },
                    1020:{ 
                        autoWidth:true,
                    },
                    1520:{                        
                        autoWidth:true,
                    }
                }
        
              } }
               aria-label="Brands We worked together"
               class=" w-[100%] z-50  "
               >
               {#each hotels as {name,url,imgUrl}}
               <SplideSlide    >
                   <div class="m-2 md:m-3 max-w-[300px] rounded-xl shadow-xl  overflow-hidden  ">
                        <img class="object-fill aspect-video  " src={imgUrl} alt={name}>
                        <div class="p-3 bg-sky-100  ">
                            <p>{name }</p>
                            <div class="flex gap-2 items-center text-sm text-black/50">
                                <span>
                                    <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24" {...$$props}>
                                        <path fill="currentColor" d="M12 11.5A2.5 2.5 0 0 1 9.5 9A2.5 2.5 0 0 1 12 6.5A2.5 2.5 0 0 1 14.5 9a2.5 2.5 0 0 1-2.5 2.5M12 2a7 7 0 0 0-7 7c0 5.25 7 13 7 13s7-7.75 7-13a7 7 0 0 0-7-7" />
                                    </svg>
                                </span>
                                <p>location</p>
                            </div>
                            <div class="flex justify-end">
                                <a href={url} class=" bg-sky-500 shadow-lg px-5 py-2 text-white  hover:bg-sky-600 rounded-full text-sm transition-all ease-in">Learn More</a>
                            </div>
                        </div>
                   </div>
               </SplideSlide>
               {/each}
            </Splide>
        </div>
    </section>
</div>