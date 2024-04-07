<script lang="ts">
    import hero_img from "$lib/assets/hero.jpg";
    import { Progressbar } from "flowbite-svelte";
</script>

<!-- Hero image -->
<div class="h-[90vh] md:h-screen flex px-20 bg-local bg-cover justify-center items-center" 
style="background-image: url({hero_img})">
    <h1 class="text-5xl leading-normal text-white text-center relative top-10">
        The Leading Destination for the very Best Healthcare Talks in Africa
    </h1>
    
    
</div>

<!-- Media player -->
<div class="relative -top-14 flex flex-col gap-2 bg-white p-6 px-8 mx-5">
    <div class="flex gap-7 items-center">
    <!-- Play button -->
        <button class="">
            <iconify-icon icon="ph:play-fill" class="bg-orange-500 hover:bg-white hover:text-orange-600 border border-orange-500 rounded-full w-fit h-fit p-6 text-white text-3xl"></iconify-icon>
        </button>
        <div>
            <h2>Talk's title</h2>
            <h3 class="text-gray-500">Episode 1. 1.27</h3>
        </div>
        
    </div>
    
    <div class="flex gap-3 items-center">
        <!-- <audio controls class="">
            <source src="" type="audio/mpeg" />
            Your browser does not support the audio element.
        </audio> -->
        <button class="rounded-full p-1 aspect-square bg-gray-100 hover:bg-orange-500 hover:text-white">-15s</button>
        <button class="rounded-full p-1 aspect-square bg-gray-100 hover:bg-orange-500 hover:text-white">+15s</button>
        <Progressbar progress="" size="h-1.5" />
        <p class="min-w-32 text-center text-gray-500"><span>00.15 / 01.27</span></p>
        <button class="text-black hover:text-white text-2xl">
            <iconify-icon icon="wpf:volume-up" class="p-3 rounded-full bg-gray-100 hover:bg-orange-500"></iconify-icon>
        </button>
    </div>
    
</div>