<script>
	import { touringPlaces } from './../constants/touringPlaces.js';
    import { Splide, SplideSlide } from '@splidejs/svelte-splide';
    // Default theme
    import '@splidejs/svelte-splide/css';
    
    
</script>
<div class="flex flex-col items-center justify-center p-5"> 
    <section class="w-full lg:w-[80%] ">
        <div>
            <h2 class="text-2xl md:text-3xl lg:text-4xl  py-5 md:p-5 font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-sky-700 to-cyan-400">Popular Touring Places</h2>
        </div>
        <div class="md:p-5">
            <Splide options={ {
                // rewind: true,
                gap   : '1rem',
                autoplay:true,
                interval: 3000, // Set the duration to 1000ms (1 second)
                // autoWidth:true,
                // wheel    : true,
                perPage: 4,
                type   : 'loop',
                pagination:false,
                drag   : 'free',
                focus  : 'start',
                autoScroll: {
                  speed: 1,
                },
                // padding: '100px',
                
                breakpoints: {
                    640:{ 
                        arrows:false,
                        autoWidth:true,
                    },
                    1020:{
                        arrows: true,
                        autoWidth:true,
                    },
                    1520:{ 
                        arrows: true,
                        autoWidth:true,
                    }
                }
        
              } }
               aria-label="Brands We worked together"
               class=" w-[100%] z-50"
               >
               {#each touringPlaces as {name,url,imgUrl}}
               <SplideSlide>
                   <div class=" max-w-[320px] relative group rounded-xl bg-slate-900/50 overflow-hidden">
                       <p class="z-[50] absolute top-0 w-full bg-sky-900/20 text-slate-900 font-extrabold text-lg p-1 px-2 ">{name}</p>
                        <a href={url} >
                            <img class="rounded object-fill aspect-video group-hover:scale-105 transition-all ease-in" src={imgUrl} alt={name}>
                            <p class=" hidden group-hover:block group-hover:absolute group-hover:bottom-2 left-2 bg-slate-900/50 px-5 py-2 text-white rounded-full text-sm transition-all ease-in">Learn More</p>
                        </a>
                   </div>
               </SplideSlide>
               {/each}
            </Splide>
        </div>
    </section>
</div>