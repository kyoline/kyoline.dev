<script>
   let value = " ";
   $: value.length > 1 ? value = value[1] : {};
   $: hex = value.charCodeAt(0).toString(16);
</script>

<div class="flex flex-row absolute justify-center items-center min-w-full">
   <input bind:value={value} class="border-2 border-black m-8 text-black" />
   <p class="font-mono">{hex}</p>
</div>