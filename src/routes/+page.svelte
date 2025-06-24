<script>
  import { icons } from "$lib/icons";
  let grayscale = false;

  function toggle() {
    grayscale = !grayscale;
  }
</script>

<div class="grid grid-flow-col grid-rows-10 m-12 gap-2">
  {#each icons as icon}
    <div class="object-contain border-gray-500">
      <button on:click={toggle}>
        <img
          class="hover:brightness-50 transition rounded hover:cursor-pointer {grayscale ? 'filter grayscale' : ''}"
          src="images/{icon.path}"
          alt="icon"
        />
      </button>
    </div>
  {/each}
</div>
