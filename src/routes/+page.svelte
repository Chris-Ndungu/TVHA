<script lang="ts">
    import Hero from "$lib/components/Hero.svelte";
    import Episodes from "$lib/components/Episodes.svelte";
    import Newsletter from "$lib/components/Newsletter.svelte";
    // import Audioplayer from "$lib/components/Audioplayer.svelte";
    // Placeholder data
    const latestEpisode = {
      title: 'My Awesome Podcast Episode',
      description: 'This is my first podcast.',
      audioUrl: 'src/lib/assets/Shenseea.mp3', // Assuming audio is in the 'public/audio' directory
      imageUrl: 'src/lib/assets/download.jpeg', // Assuming image is in the 'public/images' directory
    };
  </script>
<main class="">
    <Hero />
    <Episodes />
    <Newsletter />
</main>
