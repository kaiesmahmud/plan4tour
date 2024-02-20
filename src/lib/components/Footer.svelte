<script>
     
    let paymentsimg = [
        {
            url : "https://www.gozayaan.com/img/icon-footer-bkash.a929cde0.svg",
            alt: "Bkash Img"
        },
        {
            url : "https://www.gozayaan.com/img/icon-payment-nagad.2e467251.svg",
            alt: "Nagad Img"
        },
        {
            url : "https://www.gozayaan.com/img/icon-payment-upay.fbd2acc5.svg",
            alt: "Upay Img"
        },
        {
            url : "https://www.gozayaan.com/img/icon-footer-visa.0cc68109.svg",
            alt: "Visa Card Img"
        },
        {
            url : "https://www.gozayaan.com/img/icon-footer-amex.a8ead788.svg",
            alt: "Amex Card Img"
        },
        {
            url : "https://www.gozayaan.com/img/icon-footer-mastercard.afdd5b7f.svg",
            alt: "Master Card Img"
        },
        {
            url : "https://www.gozayaan.com/img/icon-payment-dbbl.0975a769.svg",
            alt: "DBBL Card Img"
        },
        
        {
            url : "https://www.gozayaan.com/img/icon-payment-union.d875933a.svg",
            alt: "Union Img"
        },
        {
            url : "https://www.gozayaan.com/img/icon-payment-tap.dcf016e9.svg",
            alt: "Tap Img"
        },
    ]
    let discoverLinksStyle="hover:underline hover:texts-white/90 transition-all ease-in"
</script>

<div class="relative flex flex-col items-center justify-center p-5 bg-slate-900 text-white/90 overflow-hidden">
    <div class='absolute w-[100px] h-[200px] md:w-[200px] md:h-[200px] gradient-04 opacity-50 md:opacity-30 top-10 right-0 gradient-animation' />
    <div class="w-full flex flex-col lg:flex-row  gap-3 ">
        <div class=" capitalize flex flex-col md:flex-row  w-full lg:w-1/2">
            <div class=" block w-full md:w-1/2 pl-5 my-5">
                <h3>Discover</h3>
                <div class="flex flex-col gap-4 p-3 md:-5">
                    <a href="/" class={discoverLinksStyle}>Home</a>
                    <a href="/" class={discoverLinksStyle}>Hotels</a>
                    <a href="/" class={discoverLinksStyle}>Places</a>
                    <a href="/" class={discoverLinksStyle}>blogs</a>
                </div>
            </div>
            <div class=" block w-full md:w-1/2  md:border-l pl-5 my-5">
                <h3>Payment Methods</h3>
                <div class=" inline-block">
                    <div class="grid grid-cols-3 gap-y-1  gap-x-3">
                        {#each paymentsimg as img }
                            <img class="w-20 h-20 rounded shadow" src={img.url} alt={img.alt}>
                        {/each}
                    </div>
                </div>
            </div>
        </div>
        <div class=" capitalize flex flex-col md:flex-row w-full lg:w-1/2">
            <div  class=" block w-full md:w-2/3 pl-5 my-5">
                <h3>Contact</h3>
                <div class="flex flex-col gap-3 my-5 lowercase">
                    <a href="mailto:plan4tour.com@gmail.com">plan4tour.com@gmail.com</a>
                    <a href="tel:+8801846576185">+8801846576185</a>
                </div>
                <div class="flex gap-5 text-4xl">
                    <a href="/" class="hover:text-blue-500 p-3 bg-slate-600 hover:bg-white rounded-full transition-all ease-in">
                        <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24" {...$$props}>
                            <path fill="currentColor" d="M22 12c0-5.52-4.48-10-10-10S2 6.48 2 12c0 4.84 3.44 8.87 8 9.8V15H8v-3h2V9.5C10 7.57 11.57 6 13.5 6H16v3h-2c-.55 0-1 .45-1 1v2h3v3h-3v6.95c5.05-.5 9-4.76 9-9.95" />
                        </svg>
                    </a>
                    <a href="/" class="hover:text-red-500 p-3 bg-slate-600 hover:bg-white rounded-full transition-all ease-in">
                        <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24" {...$$props}>
                            <g fill="none" fill-rule="evenodd">
                                <path d="M24 0v24H0V0zM12.593 23.258l-.011.002l-.071.035l-.02.004l-.014-.004l-.071-.035c-.01-.004-.019-.001-.024.005l-.004.01l-.017.428l.005.02l.01.013l.104.074l.015.004l.012-.004l.104-.074l.012-.016l.004-.017l-.017-.427c-.002-.01-.009-.017-.017-.018m.265-.113l-.013.002l-.185.093l-.01.01l-.003.011l.018.43l.005.012l.008.007l.201.093c.012.004.023 0 .029-.008l.004-.014l-.034-.614c-.003-.012-.01-.02-.02-.022m-.715.002a.023.023 0 0 0-.027.006l-.006.014l-.034.614c0 .012.007.02.017.024l.015-.002l.201-.093l.01-.008l.004-.011l.017-.43l-.003-.012l-.01-.01z" />
                                <path fill="currentColor" d="M12 4c.855 0 1.732.022 2.582.058l1.004.048l.961.057l.9.061l.822.064a3.802 3.802 0 0 1 3.494 3.423l.04.425l.075.91c.07.943.122 1.971.122 2.954c0 .983-.052 2.011-.122 2.954l-.075.91c-.013.146-.026.287-.04.425a3.802 3.802 0 0 1-3.495 3.423l-.82.063l-.9.062l-.962.057l-1.004.048A61.59 61.59 0 0 1 12 20a61.59 61.59 0 0 1-2.582-.058l-1.004-.048l-.961-.057l-.9-.062l-.822-.063a3.802 3.802 0 0 1-3.494-3.423l-.04-.425l-.075-.91A40.662 40.662 0 0 1 2 12c0-.983.052-2.011.122-2.954l.075-.91c.013-.146.026-.287.04-.425A3.802 3.802 0 0 1 5.73 4.288l.821-.064l.9-.061l.962-.057l1.004-.048A61.676 61.676 0 0 1 12 4m-2 5.575v4.85c0 .462.5.75.9.52l4.2-2.425a.6.6 0 0 0 0-1.04l-4.2-2.424a.6.6 0 0 0-.9.52Z" />
                            </g>
                        </svg>
                    </a>
                    <a href="/" class="hover:text-pink-500 p-3 bg-slate-600 hover:bg-white rounded-full transition-all ease-in">
                        <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24" {...$$props}>
                            <path fill="currentColor" d="M7.8 2h8.4C19.4 2 22 4.6 22 7.8v8.4a5.8 5.8 0 0 1-5.8 5.8H7.8C4.6 22 2 19.4 2 16.2V7.8A5.8 5.8 0 0 1 7.8 2m-.2 2A3.6 3.6 0 0 0 4 7.6v8.8C4 18.39 5.61 20 7.6 20h8.8a3.6 3.6 0 0 0 3.6-3.6V7.6C20 5.61 18.39 4 16.4 4zm9.65 1.5a1.25 1.25 0 0 1 1.25 1.25A1.25 1.25 0 0 1 17.25 8A1.25 1.25 0 0 1 16 6.75a1.25 1.25 0 0 1 1.25-1.25M12 7a5 5 0 0 1 5 5a5 5 0 0 1-5 5a5 5 0 0 1-5-5a5 5 0 0 1 5-5m0 2a3 3 0 0 0-3 3a3 3 0 0 0 3 3a3 3 0 0 0 3-3a3 3 0 0 0-3-3" />
                        </svg>
                    </a>
                </div>
            </div>
            <div  class=" block w-full md:w-1/3 pl-5 md:border-l my-5">
                <h3>Need Help?</h3>
                <p class="p-5">We are Always here for you! Knock us on Messenger anytime or Call our Hotline (10AM - 10PM).</p>
            </div>
        </div>
    </div>
    <footer class="flex flex-wrap justify-between items-center w-full text-cyan-500">
        <p class="font-light  text-xl">Plan4Tour.com</p>
        <p class="text-sm">
            Copyright 2023 All Right Reserved !
        </p>
    </footer>
</div>