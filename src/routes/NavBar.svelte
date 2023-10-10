<!-- NavBar.svelte -->
<nav class="pl-10">
  <div class="flex mt-">
    <button
      class="bg-transparent hover:bg-blue-700 text-white hover-orange text-xl font-bold py-5 px-8 rounded mr-8 font-heading"
      on:click={() => (window.location.href = "/")}>Home</button
    >
    <button
      class="bg-transparent hover:bg-blue-700 text-white hover-orange text-xl font-bold py-5 px-8 rounded mr-8 font-heading"
      on:click={() => (window.location.href = "/")}>Pricing</button
    >
    <button
      class="bg-transparent hover:bg-blue-700 text-white hover-orange text-xl font-bold py-5 px-8 rounded mr-8 font-heading"
      on:click={() => (window.location.href = "/")}>About</button
    >
    <button
      class="bg-transparent hover:bg-blue-700 text-white hover-orange text-xl font-bold py-5 px-8 rounded mr-8 font-heading"
      on:click={() => (window.location.href = "/")}>Resources</button
    >
    <button
      class="bg-transparent hover:bg-blue-700 text-white hover-orange text-xl font-bold py-5 px-8 rounded mr-8 font-heading"
      on:click={() => (window.location.href = "/")}>Contact</button
    >
  </div>
</nav>

<style>
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

</style>
