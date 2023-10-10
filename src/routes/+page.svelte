<script>
    import { onMount } from "svelte";
    import NavBar from "./NavBar.svelte"; // Import the NavBar component
    import Footer from "./Footer.svelte";


    let fadeIn = false;

    onMount(() => {
        // Trigger the fade-in effect when the component mounts
        fadeIn = true;
    });
</script>

<div class="{fadeIn ? 'content' : ''} flex flex-col items-center bg-gradient-to-b from-blue-900 to-blue-300" >
        <div class="icon-container">
            <img src="/lock.png" alt="Icon" class="icon" />
        </div>
        <NavBar />
        <img
            src="/lock.png"
            alt="Company Logo"
            class="w-48 h-48 rounded-full mb-10 mt-10"
        />
        <h1 class="text-9xl transition-opacity font-bold font-cool text-white fade-in-text">
            SecureIt
        </h1>
        <h2 class="text-2xl font-nav transition-opacity text-white mt-10">
            Figure out the weaknesses with your passwords to better secure your
            sensitive data
        </h2>
        <h2 class="text-xl font-nav italic text-white transition-opacity mt-10">
            Download now!
        </h2>

        <div class="flex mt-10">
            <button
                class="font-heading bg-blue-900 hover-orange text-white text-xl py-5 px-8 rounded mr-8"
                on:click={() =>
                    (window.location.href =
                        "https://drive.google.com/file/d/1VKEL9CDWW0JbDdAcAtbepBCXBwIR8zZi/view?usp=drive_link")}
            >
                Check Our Reviews
            </button>
            <button
                class="font-heading bg-blue-900 hover-orange text-white text-xl py-5 px-8 rounded mr-8"
                on:click={() =>
                    (window.location.href =
                        "https://drive.google.com/file/d/1VKEL9CDWW0JbDdAcAtbepBCXBwIR8zZi/view?usp=drive_link")}
            >
                Download App
            </button>
            <button
                class="font-heading bg-blue-900 hover-orange text-white text-xl py-5 px-8 rounded mr-8"
                on:click={() =>
                    (window.location.href =
                        "https://drive.google.com/file/d/1VKEL9CDWW0JbDdAcAtbepBCXBwIR8zZi/view?usp=drive_link")}
            >
                Chrome Extension
            </button>
        </div>
        <form class="mt-10 w-96">
            <form class="mt-8">
                <h2 class="text-2xl font-heading text-white font-i mt-10 ml-10 mb-10">
                    Questions? Reach out here
                </h2>
                <div class="mb-4">
                    <label
                        for="name"
                        class="block text-black text-sm font-bold mb-2"
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
                        class="block text-black text-sm font-bold mb-2"
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
                        class="block text-black text-sm font-bold mb-2"
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
                        class="font-heading bg-blue-900 mb-4 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline"
                    >
                        Send Message
                    </button>
                </div>
            </form>
        </form>
    <Footer />
</div>

<style>
    @keyframes fadeInAnimation {
        from {
            opacity: 0;
        }
        to {
            opacity: 1;
        }
    }

    /* Apply the animation to the content when fadeIn is true */
    .content {
        animation: fadeInAnimation 2s ease-in-out;
    }

    @font-face {
        font-family: "Bebas-Neue";
        src: url("/src/fonts/BebasNeue-Regular.ttf") format("truetype");
    }

    .font-cool {
        font-family: "Bebas-Neue";
    }

    @font-face {
        font-family: "navbar";
        src: url("/src/fonts/Aileron-Black.otf") format("truetype");
    }

    .font-nav {
        font-family: "navbar";
    }

    .hover-orange:hover {
    color: #f5c16f;
    }

    @font-face {
        font-family: "headings";
        src: url("/src/fonts/Raleway-Bold.ttf") format("truetype");
    }

    .font-heading {
        font-family: "headings";
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
