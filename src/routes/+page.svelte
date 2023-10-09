<script>
    import { onMount } from "svelte";
    import NavBar from "./NavBar.svelte"; // Import the NavBar component

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

<div class="flex flex-col items-center h-screen">
    {#if isVisible}
        <div class="icon-container">
            <img src="../src/pics/lock.png" alt="Icon" class="icon" />
          </div>
        <NavBar />
        <img
            src="/src/pics/lock.png"
            alt="Company Logo"
            class="w-48 h-48 rounded-full mb-10 mt-10"
        />
        <h1 class="text-8xl transition-opacity font-bold font-cool">
            SecureIt
        </h1>
        <h2 class="text-2xl font-sans font-bold transition-opacity mt-10">
            Figure out the weaknesses with your passwords to better secure your
            sensitive data
        </h2>
        <h2 class="text-xl font-sans italic transition-opacity mt-10">
            Download now!
        </h2>

        <div class="flex mt-10">
            <button
                class="bg-blue-500 hover:bg-blue-700 text-white text-xl font-bold py-5 px-8 rounded mr-8"
                on:click={() =>
                    (window.location.href =
                        "https://drive.google.com/file/d/1VKEL9CDWW0JbDdAcAtbepBCXBwIR8zZi/view?usp=drive_link")}
            >
                Check Our Reviews
            </button>
            <button
                class="bg-blue-500 hover:bg-blue-700 text-white text-xl font-bold py-5 px-8 rounded mr-8"
                on:click={() =>
                    (window.location.href =
                        "https://drive.google.com/file/d/1VKEL9CDWW0JbDdAcAtbepBCXBwIR8zZi/view?usp=drive_link")}
            >
                Download App
            </button>
            <button
                class="bg-blue-500 hover:bg-blue-700 text-white text-xl font-bold py-5 px-8 rounded mr-8"
                on:click={() =>
                    (window.location.href =
                        "https://drive.google.com/file/d/1VKEL9CDWW0JbDdAcAtbepBCXBwIR8zZi/view?usp=drive_link")}
            >
                Chrome Extension
            </button>
        </div>
        <form class="mt-10 w-96">
            <form class="mt-8">
                <h2 class="text-2xl font-bold font-i mt-10 ml-10 mb-10">
                    Questions? Reach out here
                </h2>
                <div class="mb-4">
                    <label
                        for="name"
                        class="block text-gray-700 text-sm font-bold mb-2"
                        >Name</label
                    >
                    <input
                        type="text"
                        id="name"
                        name="name"
                        class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                        placeholder="Your Name"
                    />
                </div>

                <div class="mb-4">
                    <label
                        for="email"
                        class="block text-gray-700 text-sm font-bold mb-2"
                        >Email</label
                    >
                    <input
                        type="email"
                        id="email"
                        name="email"
                        class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                        placeholder="Your Email"
                    />
                </div>

                <div class="mb-4">
                    <label
                        for="message"
                        class="block text-gray-700 text-sm font-bold mb-2"
                        >Message</label
                    >
                    <textarea
                        id="message"
                        name="message"
                        class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
                        rows="4"
                        placeholder="Your Message"
                    />
                </div>

                <div class="flex items-center justify-center">
                    <button
                        type="submit"
                        class="bg-blue-500 mb-4 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline"
                    >
                        Send Message
                    </button>
                </div>
            </form>
        </form>
    {/if}
</div>

<style>
    /* Define styles for your text element */
    .fade-in-text {
        opacity: 0;
        transition: opacity 0.5s ease-in-out;
    }

    @font-face {
        font-family: "Overpass-Light";
        src: url("/src/fonts/Overpass-Light.ttf") format("truetype");
    }

    .font-cool {
        font-family: "Overpass-Light";
    }

    .icon-container {
    position: absolute;
    top: 20px; /* Adjust the top position as needed */
    left: 20px; /* Adjust the left position as needed */
    z-index: 1000; /* Ensure the icon is above other elements */
  }

  .icon {
    width: 70px; /* Adjust the width and height as needed */
    height: 70px;
  }
</style>
