<script>
	import { theme } from '../../stores';
</script>

<style>
   :global(body),
   :global(html) {
      transition: background 150ms ease;
   }

   :global(::selection) {
      background: #f38ba8;
      color: #11111b;
   }
</style>
<div class:dark={$theme} class:light={!$theme}>
   <div class="dark:bg-black dark:text-white min-h-screen min-w-full bg-white text-black">
      <button on:click={() => $theme = !$theme}>theme toggle</button>
      <slot />
   </div>
</div>