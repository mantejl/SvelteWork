<script>
    import { onMount } from "svelte";
    import { library, dom } from "@fortawesome/fontawesome-svg-core";
    import { faTwitter, faInstagram, faLinkedin } from "@fortawesome/free-brands-svg-icons";
    import { faEnvelope } from "@fortawesome/free-solid-svg-icons";

    // Add the imported icons to the library
    library.add(faTwitter, faInstagram, faLinkedin, faEnvelope);

    onMount(() => {
        // Initialize the DOM to render the icons
        dom.watch();
    });
</script>

<footer class="text-black py-4">
    <div class="flex justify-center">
        <a href="https://www.twitter.com" class="mr-4 text-xl">
            <i class="fab fa-twitter"></i> <!-- Use the Font Awesome class here -->
        </a>
        <a href="https://www.instagram.com" class="mr-4 text-xl">
            <i class="fab fa-instagram"></i> <!-- Use the Font Awesome class here -->
        </a>
        <a href="https://www.google.com" class="mr-4 text-xl">
            <i class="fas fa-envelope"></i> <!-- Use the Font Awesome class here -->
        </a>
        <a href="https://www.linkedin.com" class="mr-4 text-xl">
            <i class="fab fa-linkedin"></i> <!-- Use the Font Awesome class here -->
        </a>
    </div>
    <p class="text-center mt-4 font-bold pr-3">© 2023 SecureIt</p>
</footer>
