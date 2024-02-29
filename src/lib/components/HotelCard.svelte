<script>
    import RateStar from "./RateStar.svelte";

    export let hotel ;

</script>
<div class="w-full lg:w-[80%] flex flex-col md:flex-row shadow-lg rounded-lg overflow-hidden bg-white ">
    <div class="w-full md:w-1/3 flex items-center justify-center">
     <img class=" w-full" src={hotel.imgUrl} alt={hotel.name} >
    </div>
    <div class="w-full md:w-2/3 p-2 flex flex-col md:flex-row ">
         <div class="w-full lg:w-2/3">
             <h3 class="font-bold text-lg lg:text-xl">{hotel.name}</h3>
             {#if hotel?.location}
                 <p class="text-xs lg:text-sm text-black/70 font-light w-full md:w-[90%] flex ">
                     <span class="mt-1">
                         <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24" {...$$props}>
                             <path fill="currentColor" d="M12 11.5A2.5 2.5 0 0 1 9.5 9A2.5 2.5 0 0 1 12 6.5A2.5 2.5 0 0 1 14.5 9a2.5 2.5 0 0 1-2.5 2.5M12 2a7 7 0 0 0-7 7c0 5.25 7 13 7 13s7-7.75 7-13a7 7 0 0 0-7-7" />
                         </svg>
                     </span>
                      {hotel.location}
                 </p>
             {/if}
             {#if hotel?.facilities}
                 <div class="flex  flex-wrap py-2 w-[90%] gap-1">
                     {#each hotel.facilities as {name,icon}}
                          <p class="text-xs flex  items-center gap-1 capitalize font-light px-2 py-1 border border-cyan-400 rounded">
                             <span>{@html icon }</span>
                             <span>{ name }</span>
                          </p>
                     {/each}
                 </div>
             {/if}
             {#if hotel?.description}
                 <p class="text-black/80 font-light">{hotel.description}</p>
             {/if}
         </div>
         <div class="w-full lg:w-1/3 flex flex-col items-center  p-1 text-center">
             <p>Hotel Reviews </p>
             <p class="flex">
                <RateStar rate={hotel?.rate} />
                <span> ({hotel?.reviews}) </span>
             </p>
             <div class=" text-center">
                 <p class="">Price Starts At</p>
                 <p class="text-red-500 text-lg font-semibold">BDT {hotel.offerPrice} </p>
                 <p class="  line-through text-black/80">BDT {hotel?.regularPrice} </p>
                 <p class="">{hotel?.discount} Discount</p>
             </div> 
             <div class="w-full flex justify-center md:flex-col  gap-2 text-center ">
                 <a href="/" class="border shadow bg-green-500 px-3 py-2   rounded-lg hover:bg-green-600">Call Now</a> 
                 <a href={hotel?.url} class="border shadow bg-blue-500 px-3 py-2   rounded-lg hover:bg-sky-600">View Details</a> 
             </div>
         </div>
    </div>
  </div>