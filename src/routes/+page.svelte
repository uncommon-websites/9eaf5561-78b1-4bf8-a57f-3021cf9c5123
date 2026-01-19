<script lang="ts">
  import Header from '$lib/components/Header.svelte';
  import Button from '$lib/components/Button.svelte';
  import PlannerIcon from '$lib/components/icons/PlannerIcon.svelte';
  import LightningIcon from '$lib/components/icons/LightningIcon.svelte';
</script>

<div class="min-h-screen bg-[#F7F8F6] text-[#2C3136] font-sans selection:bg-[#E6EEF1]">
  <Header />

  <main class="flex flex-col items-center w-full">
    <!-- Hero Section -->
    <section class="flex flex-col items-center justify-center text-center h-screen px-4 max-w-5xl mx-auto">
      <h2 class="text-xs font-bold uppercase tracking-[0.2em] text-primary-600 mb-6">Yearly Clarity</h2>
      
      <h1 class="text-5xl md:text-8xl font-bold tracking-tighter leading-[0.95] mb-10">
        <div class="flex flex-wrap justify-center items-center gap-x-4 gap-y-2">
          <span>Yearly</span>
          <span class="inline-flex items-center justify-center w-12 h-12 md:w-20 md:h-20 bg-gray-950 rounded-2xl align-middle mx-1">
            <PlannerIcon className="w-6 h-6 md:w-10 md:h-10 text-primary-400" />
          </span>
          <span>clarity</span>
        </div>
        <div class="flex flex-wrap justify-center items-center gap-x-4 gap-y-2">
          <span>in a single</span>
          <span class="inline-flex items-center justify-center w-12 h-12 md:w-20 md:h-20 bg-primary-500 rounded-full align-middle mx-1">
            <LightningIcon className="w-6 h-6 md:w-10 md:h-10 text-white" />
          </span>
          <span>glance</span>
        </div>
      </h1>

      <p class="text-xl md:text-2xl text-gray-500 max-w-2xl mb-12 font-medium leading-relaxed">
        Plan your year without drowning in day-to-day noise. See your entire life on one AI-assisted grid.
      </p>

      <div>
        <Button className="px-8 py-4 text-lg">
          <span class="text-base">Start planning — no signup required</span>
        </Button>
      </div>
    </section>

    <!-- Footer -->
    <footer class="w-full py-16 flex flex-col items-center gap-8 text-center border-t border-gray-100 mt-auto">
      <div class="font-bold text-2xl tracking-tight flex items-center gap-2">
        <div class="w-6 h-6 bg-black rounded flex items-center justify-center">
          <div class="w-3 h-3 bg-primary-400 rounded-sm"></div>
        </div>
        YearGrid
      </div>
      <div class="flex flex-wrap justify-center gap-8 text-sm text-gray-500 font-semibold">
        <a href="#" class="hover:text-primary-600 transition-colors">Web App</a>
        <a href="#" class="hover:text-primary-600 transition-colors">Privacy</a>
        <a href="#" class="hover:text-primary-600 transition-colors">Terms</a>
        <a href="#" class="hover:text-primary-600 transition-colors">Contact</a>
      </div>
      <div class="text-xs text-gray-300 font-medium tracking-widest uppercase">
        Built for the long-range planner
      </div>
    </footer>
  </main>
</div>
