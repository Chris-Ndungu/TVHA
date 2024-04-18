<script lang="ts">
	import hero_img from '$lib/assets/hero.jpg';
	import { Progressbar } from 'flowbite-svelte';

	// Carousel
	import { Splide, SplideSlide, SplideTrack } from '@splidejs/svelte-splide';
	import { generateSlides } from '../../utils/GenerateSlides/generateSlides';

	const slides = generateSlides();
	const options = {
		rewind: true,
		gap: '1rem',
		autoplay: true,
		arrows: true,
		height: '70vh'
	};
</script>

<section class="flex flex-col md:flex-row flex-1">
	<!-- Text -->
	<div class="bg-blue-400 h-[90vh] w-full flex px-20 bg-local bg-cover justify-center items-center">
		<h1 class="text-3xl md:text-5xl leading-loose text-orange-600 text-center relative top-10">
			The Leading Destination for the very Best Healthcare Talks in Africa
		</h1>
	</div>

	<!-- Carousel -->
	<div class="wrapper w-full">
		<h2 id="autoplay-example-heading">Autoplay</h2>

		<Splide {options} hasTrack={false} aria-labelledby="autoplay-example-heading">
			<div style="position: relative">
				<SplideTrack>
					{#each slides as slide}
						<SplideSlide>
							<img src={slide.src} alt={slide.alt} />
						</SplideSlide>
					{/each}
				</SplideTrack>
			</div>
		</Splide>
	</div>
</section>
