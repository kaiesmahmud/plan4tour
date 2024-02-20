<script>
    import { Splide, SplideSlide } from '@splidejs/svelte-splide';
    // Default theme
    import '@splidejs/svelte-splide/css';

    const specialOffers = [
        {
            name:"SEA PEARL BEACH RESORT & SPA",
            imgUrl: "https://www.amybd.com/ppscan/hotelmain/hotelmain-13-3_0708123306385.jpg",
            price: "9,554",
            location:"Jaliapalong, Inani, Ukhia, Cox’s Bazar - 4750, Bangladesh"
        },
        {
            name:"MOTEL UPAL",
            imgUrl: "https://www.amybd.com/ppscan/hotelmain/hotelmain-8-76_2106124129807.jpg",
            price: "1,500",
            location:"Motel Road, Opposite Stadium, Coxs Bazar 4700 , Bangladesh."
        },
        {
            name:"MOTEL UPAL",
            imgUrl: "https://www.amybd.com/ppscan/hotelmain/hotelmain-8-76_2106124129807.jpg",
            price: "1,500",
            location:"Motel Road, Opposite Stadium, Coxs Bazar 4700 , Bangladesh."
        },
        {
            name:"MOTEL UPAL",
            imgUrl: "https://www.amybd.com/ppscan/hotelmain/hotelmain-8-76_2106124129807.jpg",
            price: "1,500",
            location:"Motel Road, Opposite Stadium, Coxs Bazar 4700 , Bangladesh."
        },
        {
            name:"SEA PEARL BEACH RESORT & SPA",
            imgUrl: "https://www.amybd.com/ppscan/hotelmain/hotelmain-13-3_0708123306385.jpg",
            price: "9,554",
            location:"Jaliapalong, Inani, Ukhia, Cox’s Bazar - 4750, Bangladesh"
        },
        {
            name:"MOTEL UPAL",
            imgUrl: "https://www.amybd.com/ppscan/hotelmain/hotelmain-8-76_2106124129807.jpg",
            price: "1,500",
            location:"Motel Road, Opposite Stadium, Coxs Bazar 4700 , Bangladesh."
        },
        {
            name:"MOTEL UPAL",
            imgUrl: "https://www.amybd.com/ppscan/hotelmain/hotelmain-8-76_2106124129807.jpg",
            price: "1,500",
            location:"Motel Road, Opposite Stadium, Coxs Bazar 4700 , Bangladesh."
        },
        {
            name:"MOTEL UPAL",
            imgUrl: "https://www.amybd.com/ppscan/hotelmain/hotelmain-8-76_2106124129807.jpg",
            price: "1,500",
            location:"Motel Road, Opposite Stadium, Coxs Bazar 4700 , Bangladesh."
        },
    ]
</script>
<div class="flex flex-col items-center justify-center">
    <div class=" relative w-full lg:w-[80%] ">
        <section class="min-h-[80vh] w-full p-5">
            <div class="w-10 aspect-square bg-green-600 rounded flex items-center justify-center"><div class="w-5 rounded-full bg-red-500 aspect-square"></div></div>
             <h2 class=" hidden lg:block text-3xl md:text-5xl lg:text-7xl font-bold w-[100%] max-lg:w-1/2 pt-3 pb-10 text-white/90">The right <br>Destination for you<br> and your family </h2>
             <h2 class=" lg:hidden text-3xl md:text-5xl lg:text-7xl font-bold w-[100%]   pt-3 pb-10 text-white/90">The right  Destination <br> for you<br> and your family </h2>
             <p class="text-white py-5 w-[80%] bg-black/50 p-3 rounded-md">Planning the perfect vacation shouldn't be stressful. Let us help you craft an unforgettable adventure tailored to your family's unique desires. Whether you seek sun-kissed beaches, vibrant cityscapes, or awe-inspiring nature, we offer a diverse range of destinations and experiences guaranteed to create lasting memories</p>

             <div class=" w-full flex items-center justify-center py-10 ]">
                <div class="w-full lg:w-[90%] flex flex-col backdrop-blur-2xl bg-white/70 shadow-lg rounded-lg p-3 lg:p-5 ">
                    <h3 class="text-xl pt-5 md:text-2xl lg:text-3xl font-bold ">Special Offers</h3>
                    <div class="text-black pt-10 pb-5 overflow-hidden">
                        <Splide options={ {
                            // rewind: true,
                            // gap   : '1rem',
                            autoplay:true,
                            arrows:false,
                            interval: 3000, // Set the duration to 1000ms (1 second)
                            // autoWidth:true,
                            wheel    : true,
                            perPage: 5,
                            type   : 'loop',
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
                           class=" w-[100%] z-50"
                           >
                           {#each specialOffers as {name,price,location,imgUrl}}
                           <SplideSlide>
                               <div class=" max-w-[220px] px-3">
                                   <p class="font-semibold">{name}</p>
                                   <p class="text-xs flex text-black/50">
                                       <span class=" text-lg">
                                           <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24" {...$$props}>
                                               <path fill="currentColor" d="M12 11.5A2.5 2.5 0 0 1 9.5 9A2.5 2.5 0 0 1 12 6.5A2.5 2.5 0 0 1 14.5 9a2.5 2.5 0 0 1-2.5 2.5M12 2a7 7 0 0 0-7 7c0 5.25 7 13 7 13s7-7.75 7-13a7 7 0 0 0-7-7" />
                                           </svg>
                                       </span>
                                       {location}</p>
                                   <img class="rounded object-fill aspect-video" src={imgUrl} alt={name}>
                                   <div class="flex justify-between items-center p-2">
                                       <p class="text-xs px-3 py-2 bg-slate-900  text-white rounded-full" >Contact Now</p>
                                       <p class="text-sm">BDT {price}</p>
                                   </div>
                               </div>
                           </SplideSlide>
                           {/each}
                        </Splide>
                    </div>
                </div>
             </div>
        </section>
        <div class=" absolute z-[-10] max-h-screen lg:max-h-[70vh] bg-black rounded-lg overflow-hidden top-0 left-0 w-full shadow-xl ">
            <div class="relative">
                <img class=" hidden lg:block object-bottom z-[-12] bg-black opacity-80 " src="https://images.unsplash.com/photo-1464037866556-6812c9d1c72e?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="sentmartin">
                <img class="lg:hidden object-bottom z-[-12] bg-black opacity-80 " src="https://images.unsplash.com/photo-1583150647472-d239652a12f5?q=80&w=2127&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="sentmartin">
                <div class=" absolute w-full h-full bg-black/50 z-0">
                </div>
             </div>
        </div>
    </div>
    
</div>