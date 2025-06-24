<script lang="ts">
	import '../app.css';
	import { icons } from '$lib/icons';
	
	let { children } = $props();
</script>

<div class="text-center bg-gray-100 top-0">
  <h1 class="text-4xl p-6 font-black">Boston icons</h1>
  <p class="italic p-6 rounded">
    check out the <strong>{icons.length}</strong> icons from Meghan's workshop!
  </p>
</div>

{@render children()}
