<script>
    const faqData = [
        {
            id:"1",
            ques: "What is the Question ?",
            ans:"This is the answer."
        },
        {
            id:"2",
            ques: "What is the Question ?",
            ans:"This is the answer."
        },
        {
            id:"3",
            ques: "What is the Question ?",
            ans:"This is the answer."
        },
        {
            id:"4",
            ques: "What is the Question ?",
            ans:"This is the answer."
        },
    ]
    $:showAns = "1"
    const handleChangeShow = (newId)=>{
        if(showAns === newId){
            showAns = "0"
        }else{
            showAns = newId
        }
    } 
</script>

<div class="flex items-center justify-center   md:p-5 ">
    <section class="w-full  p-2 lg:w-[75%] flex flex-col items-center justify-center  bg-gradient-to-r from-sky-500 to-teal-500 md:rounded-xl md:my-10">
        <div class="w-full md:w-[90%] lg:w-[70%] flex flex-col gap-5 pb-5">
            <h3 class="text-2xl md:text-3xl lg:text-4xl   p-5 font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-sky-900 to-cyan-800 text-center">Frequently Asked Questions</h3>
            {#each faqData as {id,ques,ans}}
                 <div class="py-5 bg-white/20 p-3 rounded-lg">
                    <button class="flex items-center justify-between w-full p-3" on:click={()=>handleChangeShow(id)}>
                        <p>{id}. {ques}</p>
                        <span>
                            {#if showAns === id }
                            <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24" {...$$props}>
                                <g fill="none" fill-rule="evenodd">
                                    <path d="M24 0v24H0V0zM12.593 23.258l-.011.002l-.071.035l-.02.004l-.014-.004l-.071-.035c-.01-.004-.019-.001-.024.005l-.004.01l-.017.428l.005.02l.01.013l.104.074l.015.004l.012-.004l.104-.074l.012-.016l.004-.017l-.017-.427c-.002-.01-.009-.017-.017-.018m.265-.113l-.013.002l-.185.093l-.01.01l-.003.011l.018.43l.005.012l.008.007l.201.093c.012.004.023 0 .029-.008l.004-.014l-.034-.614c-.003-.012-.01-.02-.02-.022m-.715.002a.023.023 0 0 0-.027.006l-.006.014l-.034.614c0 .012.007.02.017.024l.015-.002l.201-.093l.01-.008l.004-.011l.017-.43l-.003-.012l-.01-.01z" />
                                    <path fill="currentColor" d="M10.94 7.94a1.5 1.5 0 0 1 2.12 0l5.658 5.656a1.5 1.5 0 1 1-2.122 2.121L12 11.122l-4.596 4.596a1.5 1.5 0 1 1-2.122-2.12z" />
                                </g>
                            </svg>                            
                            {:else}
                                <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24" {...$$props}>
                                    <g fill="none" fill-rule="evenodd">
                                        <path d="M24 0v24H0V0zM12.593 23.258l-.011.002l-.071.035l-.02.004l-.014-.004l-.071-.035c-.01-.004-.019-.001-.024.005l-.004.01l-.017.428l.005.02l.01.013l.104.074l.015.004l.012-.004l.104-.074l.012-.016l.004-.017l-.017-.427c-.002-.01-.009-.017-.017-.018m.265-.113l-.013.002l-.185.093l-.01.01l-.003.011l.018.43l.005.012l.008.007l.201.093c.012.004.023 0 .029-.008l.004-.014l-.034-.614c-.003-.012-.01-.02-.02-.022m-.715.002a.023.023 0 0 0-.027.006l-.006.014l-.034.614c0 .012.007.02.017.024l.015-.002l.201-.093l.01-.008l.004-.011l.017-.43l-.003-.012l-.01-.01z" />
                                        <path fill="currentColor" d="M13.06 16.06a1.5 1.5 0 0 1-2.12 0l-5.658-5.656a1.5 1.5 0 1 1 2.122-2.121L12 12.879l4.596-4.596a1.5 1.5 0 0 1 2.122 2.12l-5.657 5.658Z" />
                                    </g>
                                </svg>
                            {/if}
                        </span>
                    </button>
                    <div class={`${showAns === id ? " block p-5 bg-white/30 rounded-lg ": " hidden "}`}>
                        {ans}
                    </div>
                 </div>
            {/each}
        </div>
    </section>
</div>