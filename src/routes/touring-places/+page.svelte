<script>
    import Faq from "../../lib/components/Faq.svelte";
    import { touringPlaces } from "../../lib/constants/touringPlaces";

    
</script>
<div class="  flex flex-col items-center justify-center p-5 md:py-10">
    <div class="flex flex-col items-center  ">
        <h2 class="text-3xl md:text-4xl lg:text-5xl text-center p-5 font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-sky-900 to-cyan-400">Your One stop Destination for crafting <br> unforgettable Travel Experiences</h2>
        <p class="p-5 w-full lg:w-2/3 text-center text-black/80">
            At Plan4tour, we believe that travel is not just about ticking off destinations, it’s about immersing yourself in new cultures, exploring hidden gems and creating memories that will last a lifetime. That’s why we’ve combined the expertise of seasonal travel agents with the passion of experienced tour guides to offer a comprehensive travel service that caters to every traveler’s needs.
        </p>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-5 w-full md:w-[90%] lg:w-[80%]">
        {#each touringPlaces as {name,url,imgUrl}} 
            <div class="   rounded-xl shadow-xl  overflow-hidden  ">
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
                    <div class="flex justify-end gap-3">
                        <a href={url} class=" bg-teal-500 shadow-lg px-5 py-2 text-white  hover:bg-teal-600 rounded-full text-sm transition-all ease-in">Contact Local Guide</a>
                        <a href={url} class=" bg-sky-500 shadow-lg px-5 py-2 text-white  hover:bg-sky-600 rounded-full text-sm transition-all ease-in">Direction</a>
                    </div>
                </div>
            </div> 
        {/each}
    </div>
</div>
<Faq/>