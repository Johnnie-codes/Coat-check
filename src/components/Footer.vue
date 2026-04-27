<script setup>
import { Instagram, Twitter, Linkedin, Mail } from 'lucide-vue-next';
</script>

<template>
  <footer class="bg-black text-white pt-20 pb-10">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 md:grid-cols-4 gap-12 mb-16">
        <div class="col-span-1 md:col-span-2">
          <a href="#" class="flex items-center gap-2 mb-6">
            <div class="w-8 h-8 rounded-lg bg-white flex items-center justify-center text-black">
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round" class="animate-[spin_4s_linear_infinite]"><path d="M5 12h14"/><path d="M12 5v14"/></svg>
            </div>
            <span class="text-xl font-black tracking-tight">Coat Check<span class="text-slate-400">+</span></span>
          </a>
          <p class="text-slate-400 max-w-sm mb-6">
            Elevating the guest experience with premium, digital-first coat check solutions for venues and events nationwide.
          </p>
          <div class="flex gap-4">
            <a href="#" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center text-white hover:bg-white hover:text-black transition-all">
              <Instagram class="w-5 h-5" />
            </a>
            <a href="#" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center text-white hover:bg-white hover:text-black transition-all">
              <Twitter class="w-5 h-5" />
            </a>
            <a href="#" class="w-10 h-10 rounded-full bg-white/10 flex items-center justify-center text-white hover:bg-white hover:text-black transition-all">
              <Linkedin class="w-5 h-5" />
            </a>
          </div>
        </div>

        <div>
          <h4 class="font-bold mb-6">Services</h4>
          <ul class="space-y-4">
            <li><a href="#" class="text-slate-400 hover:text-white transition-colors">Venue Partnerships</a></li>
            <li><a href="#" class="text-slate-400 hover:text-white transition-colors">Private Events & Galas</a></li>
            <li><a href="#" class="text-slate-400 hover:text-white transition-colors">Corporate Events</a></li>
            <li><a href="#" class="text-slate-400 hover:text-white transition-colors">Hardware Rental</a></li>
          </ul>
        </div>

        <div>
          <h4 class="font-bold mb-6">Contact</h4>
          <ul class="space-y-4">
            <li class="flex items-center gap-3 text-slate-400">
              <Mail class="w-5 h-5 text-white" />
              <a href="mailto:hello@coatcheckplus.com" class="hover:text-white transition-colors">hello@coatcheckplus.com</a>
            </li>
            <li>
              <a href="#contact" class="inline-block mt-4 px-6 py-2 rounded-full border border-white/20 text-white hover:bg-white hover:text-black transition-colors font-bold">
                Request a Quote
              </a>
            </li>
          </ul>
        </div>
      </div>

      <div class="border-t border-white/10 pt-8 flex flex-col md:flex-row justify-between items-center gap-4">
        <p class="text-slate-500 text-sm">
          &copy; {{ new Date().getFullYear() }} Coat Check+ Inc. All rights reserved.
        </p>
        <div class="flex gap-6 text-sm">
          <a href="#" class="text-slate-500 hover:text-white transition-colors">Privacy Policy</a>
          <a href="#" class="text-slate-500 hover:text-white transition-colors">Terms of Service</a>
        </div>
      </div>
    </div>
  </footer>
</template>
