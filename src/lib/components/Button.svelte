<script lang="ts">
  import { onMount } from 'svelte';
  
  export let variant: 'primary' | 'black' = 'primary';
  export let className = '';
</script>

<button 
  class="
    inline-flex items-center justify-center gap-2 rounded-full px-5 py-2.5 text-sm font-medium transition-all active:scale-95
    {variant === 'primary' ? 'bg-[#2C3136] text-[#F7F8F6] hover:bg-[#70787F]' : ''}
    {variant === 'black' ? 'bg-[#2C3136] text-[#F7F8F6] hover:bg-[#70787F]' : ''}
    {className}
  "
>
  <slot />
</button>
