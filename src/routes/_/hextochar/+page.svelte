<script>
   let value = " ";
   $: value = value.replace(/[g-zA-Z\W_]/g, "");
   $: value.length > 2 ? value = value.slice(1) : {};
   $: char = String.fromCharCode(parseInt(value, 16));
</script>

<div class="flex flex-row min-w-full absolute justify-center items-center">
   <input bind:value={value} class="border-2 border-black m-8 text-black" />
   <p class="font-mono">{char}</p>
</div>