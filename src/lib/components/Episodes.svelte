<script lang="ts">
    import 'iconify-icon';
    import cover from '$lib/assets/cover.png';
</script>


<section class="mx-5 pb-20">
    <div class="flex flex-col gap-8">
        <div>
            <h3 class="text-orange-600 text-2xl">Enjoy New Shows</h3>
            <h1 class="text-4xl">Latest talks</h1>
        </div>

        <!-- Episodes -->
        <div class="flex">
            <div class=" shadow-md flex flex-col w-screen">
                <img src="{cover}" alt="Latest Episode Artwork" class="w-full">
                <div class="mx-8 my-3 flex flex-col gap-3 border-t p-6">
                    <div class="flex items-center gap-4">
                        <iconify-icon icon="material-symbols:headphones-outline" class="text-white text-xl p-3 border border-transparent bg-orange-500 rounded-full"></iconify-icon>

                        <h4 class="text-orange-500 text-xl">Episode Type</h4> 
                        <p class="text-gray-500">Episode 1</p>               
                    </div>
                    <h5>Episode title</h5>
                    <a href="" class="hover:text-orange-600 text-xs">VIEW EPISODE &RightArrow;</a>
                </div>
            </div>
            <!--  -->
            <div class=" shadow-md hidden aria-hidden:hidden md:flex md:flex-col w-screen">
                <img src="{cover}" alt="Latest Episode Artwork" class="w-full"> 
                <div class="mx-8 my-3 flex flex-col gap-3 border-t p-6">
                    <div class="flex items-center gap-4">
                        <iconify-icon icon="material-symbols:headphones-outline" class="text-white text-xl p-3 border border-transparent bg-orange-500 rounded-full"></iconify-icon>

                        <h4 class="text-orange-500 text-xl">Episode Type</h4> 
                        <p class="text-gray-500">Episode 1</p>               
                    </div>
                    <h5>Episode title</h5>
                    <a href="" class="hover:text-orange-600 text-xs">VIEW EPISODE &RightArrow;</a>
                </div>
            </div>
            <!--  -->
            <div class=" shadow-md hidden aria-hidden:hidden lg:flex lg:flex-col w-screen">
                <img src="{cover}" alt="Latest Episode Artwork" class="w-full"> 
                <div class="mx-8 my-3 flex flex-col gap-3 border-t p-6">
                    <div class="flex items-center gap-4">
                        <iconify-icon icon="material-symbols:headphones-outline" class="text-white text-xl p-3 border border-transparent bg-orange-500 rounded-full"></iconify-icon>

                        <h4 class="text-orange-500 text-xl">Episode Type</h4> 
                        <p class="text-gray-500">Episode 1</p>               
                    </div>
                    <h5>Episode title</h5>
                    <a href="" class="hover:text-orange-600 text-xs">VIEW EPISODE &RightArrow;</a>
                </div>
            </div>
        </div>

    </div>    
</section>