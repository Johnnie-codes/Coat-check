<script setup>
import { ShieldCheck, Zap, Ticket } from 'lucide-vue-next';
</script>

<template>
  <section class="relative pt-32 pb-20 lg:pt-48 lg:pb-32 overflow-hidden bg-white">
    <!-- Background Elements -->
    <div class="absolute inset-0 z-0">
      <div class="absolute top-0 left-1/2 -translate-x-1/2 w-[1000px] h-[500px] bg-slate-100 rounded-full blur-[120px] opacity-70 pointer-events-none"></div>
      <div class="absolute bottom-0 right-0 w-[600px] h-[600px] bg-slate-50 rounded-full blur-[100px] pointer-events-none"></div>
      <div class="absolute inset-0 bg-[url('https://grainy-gradients.vercel.app/noise.svg')] opacity-[0.03] pointer-events-none"></div>
    </div>

    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
      <div class="grid lg:grid-cols-2 gap-12 lg:gap-8 items-center">
        <!-- Hero Content -->
        <div class="max-w-2xl">
          <div class="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-slate-100 border border-slate-200 text-slate-700 text-sm font-semibold mb-6 animate-fade-in-up">
            <span class="relative flex h-2 w-2">
              <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-slate-400 opacity-75"></span>
              <span class="relative inline-flex rounded-full h-2 w-2 bg-black"></span>
            </span>
            Now serving venues nationwide
          </div>
          
          <h1 class="text-5xl lg:text-7xl font-black tracking-tight mb-6 animate-fade-in-up delay-100 text-black leading-[1.1]">
            Elevate Your <br>
            <span class="text-slate-500">Event Experience</span>
          </h1>
          
          <p class="text-lg lg:text-xl text-slate-600 mb-8 leading-relaxed animate-fade-in-up delay-200">
            Premium coat check services for parties, galas, and venues. Digital tickets, zero lost items, and lightning-fast retrieval times.
          </p>
          
          <div class="flex flex-col sm:flex-row gap-4 animate-fade-in-up delay-300">
            <a href="#contact" class="inline-flex justify-center items-center gap-2 px-8 py-4 rounded-full bg-black hover:bg-slate-800 text-white font-bold transition-all hover:scale-105 shadow-xl shadow-black/10">
              Book Our Services
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
            </a>
            <a href="#how-it-works" class="inline-flex justify-center items-center gap-2 px-8 py-4 rounded-full bg-white border-2 border-slate-200 hover:border-black text-black font-bold transition-all">
              See How It Works
            </a>
          </div>

          <!-- Trust Badges -->
          <div class="mt-12 flex items-center gap-6 text-sm text-slate-500 font-medium animate-fade-in-up delay-300">
            <div class="flex items-center gap-2">
              <ShieldCheck class="w-5 h-5 text-black" />
              <span>Fully Insured</span>
            </div>
            <div class="flex items-center gap-2">
              <Zap class="w-5 h-5 text-black" />
              <span>Fast Retrieval</span>
            </div>
            <div class="flex items-center gap-2">
              <Ticket class="w-5 h-5 text-black" />
              <span>Paperless</span>
            </div>
          </div>
        </div>

        <!-- Hero Visual (Interactive/Abstract) -->
        <div class="relative lg:h-[600px] flex items-center justify-center animate-fade-in-up delay-200">
          <!-- Main visual container -->
          <div class="relative w-full max-w-md aspect-[4/5] rounded-3xl bg-white p-2 shadow-2xl border border-slate-200 transform rotate-2 hover:rotate-0 transition-transform duration-500 group">
            <div class="absolute inset-0 bg-slate-50 rounded-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            
            <div class="w-full h-full rounded-2xl bg-slate-50 overflow-hidden relative border border-slate-200">
              <!-- Mock App Interface -->
              <div class="absolute top-0 w-full p-6 border-b border-slate-200 bg-white/80 backdrop-blur">
                <div class="flex justify-between items-center mb-6">
                  <div class="w-8 h-8 rounded-full bg-slate-200 flex items-center justify-center">
                    <div class="w-4 h-4 bg-black rounded-full"></div>
                  </div>
                  <div class="text-sm font-bold text-slate-900">Ticket ID</div>
                </div>
                <div class="w-full h-48 bg-white rounded-xl flex items-center justify-center p-4 border border-slate-100 shadow-sm">
                  <!-- Mock QR Code -->
                  <div class="w-full h-full bg-[url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMDAgMTAwIj48cGF0aCBmaWxsPSIjMDAwIiBkPSJNMCAwaDQwdjQwaC00MHpNNjAgMGg0MHY0MGgtNDB6TTAgNjBoNDB2NDBoLTQwek0xMCAxMGgyMHYyMGgtMjB6TTcwIDEwaDIwdjIwaC0yMHpNMTAgNzBoMjB2MjBoLTIweiIvPjxyZWN0IHdpZHRoPSIxMCIgaGVpZ2h0PSIxMCIgeD0iMTAiIHk9IjEwIiBmaWxsPSIjMDAwIi8+PHJlY3Qgd2lkdGg9IjEwIiBoZWlnaHQ9IjEwIiB4PSI3MCIgeT0iMTAiIGZpbGw9IiMwMDAiLz48cmVjdCB3aWR0aD0iMTAiIGhlaWdodD0iMTAiIHg9IjEwIiB5PSI3MCIgZmlsbD0iIzAwMCIvPjxwYXRoIGZpbGw9IiMwMDAiIGQ9Ik01MCAwaDEwdjEwaC0xMHpNNTAgMjBoMTB2MTBoLTEwek01MCA0MGgxMHYxMGgtMTB6TTUwIDYwaDEwdjEwaC0xMHpNNTAgODBoMTB2MTBoLTEwek0yMCA1MGgxMHYxMGgtMTB6TTcwIDcwaDEwdjEwaC0xMHpNMzAgMzBoMTB2MTBoLTEwek04MCAzMGgxMHYxMGgtMTB6Ii8+PC9zdmc+')] bg-no-repeat bg-contain bg-center opacity-90"></div>
                </div>
                <div class="mt-6 text-center">
                  <p class="text-slate-500 text-sm mb-1 font-medium">Items Checked</p>
                  <p class="text-xl font-black text-black">Black Trench Coat</p>
                </div>
                <div class="mt-8 flex justify-center">
                   <div class="px-6 py-2 rounded-full bg-slate-100 border border-slate-200 text-slate-800 text-sm font-bold flex items-center gap-2">
                     <span class="w-2 h-2 rounded-full bg-black animate-pulse"></span>
                     Ready for pickup
                   </div>
                </div>
              </div>
            </div>
            
            <!-- Floating Elements -->
            <div class="absolute -right-12 top-20 bg-white px-4 py-3 rounded-2xl border border-slate-200 shadow-xl flex items-center gap-3 animate-bounce" style="animation-duration: 3s;">
              <div class="w-10 h-10 rounded-full bg-slate-100 flex items-center justify-center text-black">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M20 6 9 17l-5-5"/></svg>
              </div>
              <div>
                <p class="text-sm font-bold text-black">Item Retrieved</p>
                <p class="text-xs text-slate-500">Just now</p>
              </div>
            </div>

            <div class="absolute -left-10 bottom-32 bg-white px-4 py-3 rounded-2xl border border-slate-200 shadow-xl flex items-center gap-3 animate-bounce" style="animation-duration: 4s; animation-delay: 1s;">
              <div class="w-10 h-10 rounded-full bg-slate-100 flex items-center justify-center text-black">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2v20"/><path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"/></svg>
              </div>
              <div>
                <p class="text-sm font-bold text-black">Generous Tip</p>
                <p class="text-xs text-slate-500">via Telebirr</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
