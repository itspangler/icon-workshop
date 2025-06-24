<script>
  import { icons } from "$lib/icons";
  // import { onMount } from "svelte";
</script>

<div class="text-center bg-gray-100 top-0">
  <h1 class="text-4xl p-6 font-black">Boston icons</h1>
  <p class="italic p-6 rounded">
    check out the <strong>{icons.length}</strong> icons from Meghan's workshop!
  </p>
</div>

<div class="grid grid-flow-col grid-rows-8 m-12 gap-2">
  {#each icons as icon}
    <container
      class="object-contain border-gray-500"
    >
    <!-- <p class="text-xs bg-gray-100 p-1 rounded mb-1 text-center">title</p> -->
      <img class="hover:brightness-50 transition rounded hover:cursor-pointer" src="../images/{icon.path}" />
    </container>
  {/each}
</div>
