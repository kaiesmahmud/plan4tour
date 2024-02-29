<script>
	import { navList } from './../constants/navlist.js';
    
    $:viewNavOptions = false;
    const handleViewNavOptions = ()=> viewNavOptions = !viewNavOptions
    const handleLogoClick = ()=> viewNavOptions = false
 </script>
<header class={`p-3 ${viewNavOptions? " h-screen ": "h-auto"} lg:h-auto  flex  flex-col lg:flex-row gap-5  lg:items-center lg:justify-between lg:px-10 `}>
    <div class="flex justify-between w-full lg:w-auto">
        <a  on:click={handleLogoClick} href="/" class="flex items-center gap-2 ">
            <img class="w-8 md:w-10 " src="/logo.webp" alt="" srcset="">
            <p class=" font_Inter text-xl md:text-2xl lg:text-3xl">Plan<span class="text-green-500">4</span>Tour</p>
        </a>
        
        <button on:click={handleViewNavOptions} class=" inline-block lg:hidden text-3xl">
            {#if viewNavOptions}
                <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24" {...$$props}>
                    <path fill="none" stroke="currentColor" stroke-linecap="round" stroke-width="2" d="M20 20L4 4m16 0L4 20" />
                </svg>
            {:else}
                <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24" {...$$props}>
                    <path fill="currentColor" d="M22 18.005c0 .55-.446.995-.995.995h-8.01a.995.995 0 0 1 0-1.99h8.01c.55 0 .995.445.995.995M22 12c0 .55-.446.995-.995.995H2.995a.995.995 0 1 1 0-1.99h18.01c.55 0 .995.446.995.995m-.995-5.01a.995.995 0 0 0 0-1.99H8.995a.995.995 0 1 0 0 1.99z" />
                </svg>
            {/if}
        </button>
    </div>
    <nav  class={`${viewNavOptions? "flex ": "hidden lg:flex "} lg:flex  flex-col lg:flex-row lg:items-center gap-3 text-sm   uppercase font_Poppins`}>
        {#each navList as {link,name}}
        <div class="flex rounded overflow-hidden" >
            <a on:click={handleViewNavOptions} href={link} class="fira-sans-semibold rounded transition-all ease-in duration-300 w-full lg:w-auto hover:text-green-600">
                <p class="p-3 rounded nav_gradient text-lg">{name}</p>
            </a>
        </div>
        {/each}
         
    </nav>
</header>