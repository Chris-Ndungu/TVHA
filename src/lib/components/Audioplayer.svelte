<!-- AudioPlayer.svelte -->
<script>
    // Define audio properties (you can modify these)
    let mediaTitle = "How to build habit in 30 days with Linda?";
    let artist = "Mike Hardson";
    let episodeNumber = 12;
    let currentTime = 15; // in seconds
    let totalDuration = 27; // in seconds
    let isPlaying = false;
    let volume = 0.7; // 0 to 1
  
    // Event handlers
    function togglePlay() {
      isPlaying = !isPlaying;
      // Implement play/pause logic here
    }
  
    function seekTo(time) {
      // Implement seeking logic here
    }
  
    function adjustVolume(newVolume) {
      // Implement volume control logic here
      volume = newVolume;
    }
  </script>
  
  <div class="audio-player">
    <button on:click={togglePlay}>
      {isPlaying ? "Pause" : "Play"}
    </button>
    <div class="media-details">
      <p>{mediaTitle}</p>
      <p>{artist} . Episode {episodeNumber} . {currentTime}:{totalDuration}</p>
    </div>
    <input
      type="range"
      min="0"
      max={totalDuration}
      value={currentTime}
      on:input={event => seekTo(event.target.value)}
    />
    <div class="time-indicators">
      <span>{currentTime}</span> / <span>{totalDuration}</span>
    </div>
    <input
      type="range"
      min="0"
      max="1"
      step="0.01"
      value={volume}
      on:input={event => adjustVolume(event.target.value)}
    />
  </div>
  
  <style>
    /* Add your custom styling here */
    .audio-player {
      /* Styling for the audio player container */
    }
    /* Other styles for buttons, progress bar, etc. */
  </style>
  