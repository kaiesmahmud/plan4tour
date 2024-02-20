<script>
	import Navbar from './../lib/components/Navbar.svelte';
    import Footer from '../lib/components/Footer.svelte';
    import "../app.css";
</script>
<div class="flex items-center justify-center  ">
    <div class=" relative w-[100vw] md:max-w-[3000px] flex flex-col  bg-slate-200 z-0   ">
        <div class=" sticky top-0 z-[100000] backdrop-blur-2xl shadow-lg">
            <Navbar/>
        </div>
        <slot />
        <Footer/>
    </div>
</div>