<script>
  import { icons } from "$lib/icons";
  let grayscale = false;

  function toggle() {
    grayscale = !grayscale;
  }
</script>

<div class="fixed top-4 right-4">
    <button onclick={toggle} class="hover:cursor-pointer z-index-5000 bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded-full box-shadow-lg {!grayscale ? 'filter grayscale' : ''}">
    🌈
  </button>
</div>

<div class="grid grid-flow-col m-12 gap-2 grid-rows-32 md:grid-rows-10">
  {#each icons as icon}
    <div class="object-contain border-gray-500">
      <a target="blank" href="/images/{icon.path}">
        <img
          class="hover:brightness-50 transition rounded hover:cursor-pointer {grayscale ? 'filter grayscale' : ''}"
          src="images/{icon.path}"
          alt="icon"
        />
      </a>
    </div>
  {/each}
</div>
