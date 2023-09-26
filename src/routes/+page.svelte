<script>
    import { onMount } from 'svelte';
    import NavBar from './NavBar.svelte'; // Import the NavBar component
  
    let isVisible = false;
  
    // This function will trigger the transition
    function fadeIn() {
      isVisible = true;
    }
  
    // Use the onMount lifecycle function to trigger fadeIn when the component is mounted
    onMount(() => {
      fadeIn();
    });
  </script>
  
<style>
    /* Define styles for your text element */
    .fade-in-text {
      opacity: 0;
      transition: opacity 0.5s ease-in-out;
    }

    @font-face{
        font-family: "Overpass-Light";
        src:url('/src/fonts/Overpass-Light.ttf') format('truetype');
    }

    .font-cool {
    font-family: 'Overpass-Light';
    }
</style> 
  
<div class="flex flex-col items-center h-screen">
    {#if isVisible}
        <NavBar />
        <img src="/src/pics/lock.png" alt="Company Logo" class="w-48 h-48 rounded-full mb-10 mt-10" />
        <h1 class="text-8xl transition-opacity font-bold font-cool">
          SecureIt
        </h1>
        <h2 class="text-2xl font-sans font-bold transition-opacity mt-10"> 
          Figure out the weaknesses with your passwords to better secure your sensitive data
        </h2>
        <h2 class="text-xl font-sans italic transition-opacity mt-10"> 
            Download now!
        </h2>
        <div class="flex mt-10">
            <button class="bg-blue-500 hover:bg-blue-700 text-white text-xl font-bold py-5 px-8 rounded mr-8"
            on:click={() => window.location.href = 'https://drive.google.com/file/d/1VKEL9CDWW0JbDdAcAtbepBCXBwIR8zZi/view?usp=drive_link'}
            >
              Check Our Reviews
            </button>
            <button class="bg-blue-500 hover:bg-blue-700 text-white text-xl font-bold py-5 px-8 rounded mr-8"
            on:click={() => window.location.href = 'https://drive.google.com/file/d/1VKEL9CDWW0JbDdAcAtbepBCXBwIR8zZi/view?usp=drive_link'}
            >
              Download App
            </button>
            <button class="bg-blue-500 hover:bg-blue-700 text-white text-xl font-bold py-5 px-8 rounded mr-8"
            on:click={() => window.location.href = 'https://drive.google.com/file/d/1VKEL9CDWW0JbDdAcAtbepBCXBwIR8zZi/view?usp=drive_link'}>
              Chrome Extension
            </button>
          </div>
    {/if}
  </div>
  
  