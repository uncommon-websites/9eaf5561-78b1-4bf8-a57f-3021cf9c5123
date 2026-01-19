<script lang="ts">
  import Button from './Button.svelte';
  import Apple from './icons/Apple.svelte';
</script>

<header class="w-full max-w-[1200px] mx-auto px-6 py-6 flex items-center justify-between">
  <div class="font-bold text-xl tracking-tight flex items-center gap-2">
    <div class="w-6 h-6 bg-black rounded flex items-center justify-center">
      <div class="w-3 h-3 bg-primary-400 rounded-sm"></div>
    </div>
    YearGrid
  </div>
  <Button>
    <span class="text-sm">Try it now</span>
  </Button>
</header>
