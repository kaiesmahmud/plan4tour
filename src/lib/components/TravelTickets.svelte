<script>
    import { Splide, SplideSlide } from '@splidejs/svelte-splide';
    // Default theme
    import '@splidejs/svelte-splide/css';
    const places = [
        {
            name:"Aquaholic Tourist Caravan", 
            url:"/",
            imgUrl: "https://plus.unsplash.com/premium_photo-1661713771405-09e2b484fdc8?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MXx8dG91ciUyMGJ1c3xlbnwwfHwwfHx8MA%3D%3D",
        },
        {
            name:"Aquaholic Tourist Caravan",
            url:"/",
            imgUrl: "https://plus.unsplash.com/premium_photo-1661713771405-09e2b484fdc8?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MXx8dG91ciUyMGJ1c3xlbnwwfHwwfHx8MA%3D%3D",
        },
        {
            name:"Aquaholic Tourist Caravan",
            url:"/",
            imgUrl: "https://plus.unsplash.com/premium_photo-1661713771405-09e2b484fdc8?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MXx8dG91ciUyMGJ1c3xlbnwwfHwwfHx8MA%3D%3D",
        },
        {
            name:"Aquaholic Tourist Caravan",
            url:"/",
            imgUrl: "https://plus.unsplash.com/premium_photo-1661713771405-09e2b484fdc8?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MXx8dG91ciUyMGJ1c3xlbnwwfHwwfHx8MA%3D%3D",
        },
        {
            name:"Aquaholic Tourist Caravan",
            url:"/",
            imgUrl: "https://plus.unsplash.com/premium_photo-1661713771405-09e2b484fdc8?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MXx8dG91ciUyMGJ1c3xlbnwwfHwwfHx8MA%3D%3D",
        },
    ]
</script>
<div class="flex flex-col items-center justify-center p-5"> 
    <section class="w-full lg:w-[80%] ">
        <div>
            <h2 class="text-2xl md:text-3xl lg:text-4xl   py-5 md:p-5 font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-sky-700 to-cyan-400">Travel Tickets</h2>
        </div>
        <div class="md:p-5">
            <Splide options={ {
                
                // type   : 'loop',
                // rewind: true,
                gap   : '1rem',
                autoplay:true,
                arrows:false,
                interval: 3000, // Set the duration to 1000ms (1 second)
                // autoWidth:true,
                wheel    : true,
                perPage: 4,
                pagination:false,
                drag   : 'free',
                focus  : 'start',
                autoScroll: {
                  speed: 1,
                },
                 
                breakpoints: {
                    640:{
                         
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
               {#each places as {name,url,imgUrl}}
               <SplideSlide    >
                   <div class="m-2 md:m-3 max-w-[300px] min-h-[200px] rounded-xl shadow-xl  overflow-hidden flex   ">
                        <img class="w-1/2 object-fill aspect-video  " src={imgUrl} alt={name}>
                        <div class="p-3 bg-sky-100 flex flex-col gap-1  justify-between">
                            <div>
                                <p>Hanif Paribohon</p>
                                <p class="text-xs text-black/50">Available: 24 Hour</p>
                                <p class="text-sm text-black/50">Dhaka - Cox's Bazar</p>
                            </div>
                            <div class="flex flex-col justify-center items-center ">
                                <p class="text-sm text-black/50">BDT 1,200</p>
                                <a href={url} class=" bg-sky-500 shadow-lg px-3 py-1 text-white  hover:bg-sky-600 rounded-full   transition-all ease-in text-sm">Buy Now</a>
                            </div>
                        </div>
                   </div>
               </SplideSlide>
               {/each}
            </Splide>
        </div>
    </section>
</div>