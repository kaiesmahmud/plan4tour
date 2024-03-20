<script>
    import Faq from '../../lib/components/Faq.svelte';
	import { travelTickets } from './../../lib/constants/travelTickets.js';

</script>
<div class="  flex flex-col items-center justify-center p-5 md:py-10">
    <div class="flex flex-col items-center  ">
        <h2 class="text-3xl md:text-4xl lg:text-5xl text-center p-5 font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-sky-900 to-cyan-400">Your One stop Destination for crafting <br> unforgettable Travel Experiences</h2>
        <p class="p-5 w-full lg:w-2/3 text-center text-black/80">
            At Plan4tour, we believe that travel is not just about ticking off destinations, it’s about immersing yourself in new cultures, exploring hidden gems and creating memories that will last a lifetime. That’s why we’ve combined the expertise of seasonal travel agents with the passion of experienced tour guides to offer a comprehensive travel service that caters to every traveler’s needs.
        </p>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-5 w-full md:w-[80%] lg:w-[70%]">
        {#each travelTickets as {name,url,imgUrl}} 
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
        {/each}
    </div>
</div>
<Faq/>