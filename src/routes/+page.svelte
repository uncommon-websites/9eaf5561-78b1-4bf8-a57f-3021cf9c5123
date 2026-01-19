<script lang="ts">
  import Header from '$lib/components/Header.svelte';
  import Button from '$lib/components/Button.svelte';
  import PlannerIcon from '$lib/components/icons/PlannerIcon.svelte';
  import LightningIcon from '$lib/components/icons/LightningIcon.svelte';
  import MindIcon from '$lib/components/icons/MindIcon.svelte';
</script>

<div class="min-h-screen bg-white text-black font-sans selection:bg-primary-100">
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

    <!-- Features Section -->
    <section class="w-full bg-gray-950 text-white py-32 px-6">
      <div class="max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-24 items-center">
        <div class="space-y-8">
          <h2 class="text-4xl md:text-6xl font-bold tracking-tight">The heatmap-style year grid</h2>
          <p class="text-xl text-gray-400 leading-relaxed">
            Traditional calendars trap you in busywork. Ours sets you free. Every day is contextual, categorized, and color-coded—from now until next December.
          </p>
          <ul class="space-y-4 text-lg">
            <li class="flex items-center gap-3">
              <div class="w-2 h-2 rounded-full bg-primary-500"></div>
              <span>Organize by work, health, family, and travel</span>
            </li>
            <li class="flex items-center gap-3">
              <div class="w-2 h-2 rounded-full bg-primary-500"></div>
              <span>Collapse complexity with sub-calendars</span>
            </li>
            <li class="flex items-center gap-3">
              <div class="w-2 h-2 rounded-full bg-primary-500"></div>
              <span>Visual filters for instant clarity</span>
            </li>
          </ul>
        </div>
        <div class="relative">
          <div class="absolute -inset-4 bg-primary-500/20 blur-3xl rounded-full"></div>
          <img 
            src="/generated/image-close-up-of-a-hand-holding-a-smartphone--1768862718697-1.webp" 
            alt="Mobile App View" 
            class="relative rounded-2xl shadow-2xl border border-white/10"
          />
        </div>
      </div>
    </section>

    <!-- AI Capture Section -->
    <section class="w-full py-32 px-6 bg-white">
      <div class="max-w-6xl mx-auto flex flex-col md:flex-row-reverse gap-24 items-center">
        <div class="flex-1 space-y-8">
          <h2 class="text-4xl md:text-6xl font-bold tracking-tight">AI-assisted capture</h2>
          <p class="text-xl text-gray-600 leading-relaxed">
            Stop manual entry. Upload screenshots of emails, flyers, or texts. Our AI extracts titles, dates, and recurrence to pre-fill your events instantly.
          </p>
          <div class="p-6 bg-gray-50 rounded-2xl border border-gray-100 flex items-start gap-4">
            <div class="w-10 h-10 bg-primary-100 rounded-lg flex items-center justify-center shrink-0">
              <MindIcon className="w-6 h-6 text-primary-600" />
            </div>
            <div>
              <h4 class="font-bold text-gray-900">Natural Language Parsing</h4>
              <p class="text-gray-500">Type "every 2nd Tuesday" and watch it map across the whole year in seconds.</p>
            </div>
          </div>
        </div>
        <div class="flex-1 bg-gray-100 rounded-[2.5rem] p-8 aspect-square flex items-center justify-center overflow-hidden">
           <div class="grid grid-cols-7 gap-2 w-full max-w-sm">
             {#each Array(49) as _, i}
               <div class="aspect-square rounded-sm {i % 7 === 0 ? 'bg-primary-400' : i % 13 === 0 ? 'bg-primary-200' : 'bg-white'} shadow-sm"></div>
             {/each}
           </div>
        </div>
      </div>
    </section>

    <!-- Privacy Section -->
    <section class="max-w-4xl mx-auto px-6 py-32 text-center space-y-12">
      <div class="inline-block px-4 py-1.5 bg-gray-100 rounded-full text-sm font-bold uppercase tracking-wider">Local-First Privacy</div>
      <h3 class="text-4xl md:text-6xl font-bold tracking-tight leading-[1.1]">
        No setup. No account. <br/>No stress.
      </h3>
      <p class="text-xl text-gray-500 max-w-2xl mx-auto leading-relaxed">
        YearGrid works instantly in your browser. Your data stays in LocalStorage, meaning we never see your schedule. Share specific calendars with lightweight links when you're ready.
      </p>
    </section>

    <!-- CTA -->
    <section class="w-full py-32 px-6 text-center">
      <div class="max-w-3xl mx-auto space-y-10">
        <h2 class="text-4xl md:text-7xl font-bold tracking-tighter">Ready for yearly clarity?</h2>
        <p class="text-xl text-gray-500">If your current calendar makes you feel behind, try one that helps you see ahead.</p>
        <div class="pt-4">
          <Button className="px-10 py-5 text-xl">
            <span class="text-lg">Start your grid now</span>
          </Button>
          <p class="mt-4 text-sm text-gray-400 font-medium">Free to use. No credit card required.</p>
        </div>
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


