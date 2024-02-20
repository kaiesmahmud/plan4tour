<script>
    import Hero from "../lib/components/Hero.svelte";
    import HotelsForBooking from "../lib/components/HotelsForBooking.svelte";
    import PopularTouringPlaces from "../lib/components/PopularTouringPlaces.svelte";


</script>
<Hero/> 
<div class="flex flex-col items-center  ">
    <h2 class="text-3xl md:text-4xl lg:text-5xl text-center p-5 font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-sky-900 to-cyan-400">Your One stop Destination for crafting <br> unforgettable Travel Experiences</h2>
    <p class="p-5 w-full lg:w-2/3 text-center text-black/80">
        At Plan4tour, we believe that travel is not just about ticking off destinations, it’s about immersing yourself in new cultures, exploring hidden gems and creating memories that will last a lifetime. That’s why we’ve combined the expertise of seasonal travel agents with the passion of experienced tour guides to offer a comprehensive travel service that caters to every traveler’s needs.
    </p>
</div>
<PopularTouringPlaces/>
<HotelsForBooking/>