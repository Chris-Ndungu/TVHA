<script lang="ts">
    import { Splide, SplideSlide, SplideTrack } from '@splidejs/svelte-splide';
    import { generateSlides } from '../../utils/GenerateSlides/generateSlides';
  
    const slides = generateSlides();
    const options = {
      rewind  : true,
      gap     : '1rem',
      autoplay: true,
      arrows  : true,
      height  : '15rem',
    }
  </script>
  
  <div class="wrapper">
    <h2 id="autoplay-example-heading">Autoplay</h2>
  
    <Splide options={ options } hasTrack={ false } aria-labelledby="autoplay-example-heading">
      <div style="position: relative">
        <SplideTrack>
          { #each slides as slide }
            <SplideSlide>
              <img src={ slide.src } alt={ slide.alt }>
            </SplideSlide>
          { /each }
        </SplideTrack>
      </div>
    </Splide>
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

  <style global>
  
    h1 {
      text-align: center;
    }
  
    hr {
      width: 200px;
      max-width: 50%;
      margin: 4rem auto;
    }
  
    button {
      font-family: inherit;
    }
  
    .wrapper {
      max-width: 600px;
      margin: 0 auto;
    }
  
    .splide__slide {
      background: #eee;
    }
  
    .splide__slide img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  
    .splide--nav {
      margin-top: 1rem;
    }
  </style>