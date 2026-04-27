<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const isScrolled = ref(false);
const isMobileMenuOpen = ref(false);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 20;
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});

const navLinks = [
  { name: 'Features', href: '#features' },
  { name: 'How It Works', href: '#how-it-works' },
  { name: 'Testimonials', href: '#testimonials' },
];
</script>

<template>
  <header 
    :class="['fixed top-0 w-full z-50 transition-all duration-300', isScrolled ? 'glass py-3' : 'bg-transparent py-5']"
  >
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center">
        <!-- Logo -->
        <div class="flex items-center">
          <a href="#" class="flex items-center gap-2 group">
            <div class="w-10 h-10 rounded-xl bg-black flex items-center justify-center text-white shadow-lg group-hover:shadow-black/20 transition-all">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round" class="animate-[spin_4s_linear_infinite]"><path d="M5 12h14"/><path d="M12 5v14"/></svg>
            </div>
            <span class="text-xl font-black tracking-tight text-slate-900 transition-colors">Coat Check<span class="text-black">+</span></span>
          </a>
        </div>

        <!-- Desktop Navigation -->
        <nav class="hidden md:flex items-center gap-8">
          <a v-for="link in navLinks" :key="link.name" :href="link.href" class="text-sm font-semibold text-slate-600 hover:text-black transition-colors">
            {{ link.name }}
          </a>
          <a href="#contact" class="px-5 py-2.5 rounded-full bg-black hover:bg-slate-800 text-white text-sm font-medium transition-all hover:scale-105 shadow-md">
            Get a Quote
          </a>
        </nav>

        <!-- Mobile Menu Button -->
        <div class="md:hidden">
          <button @click="isMobileMenuOpen = !isMobileMenuOpen" class="text-slate-900 p-2">
            <svg v-if="!isMobileMenuOpen" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="4" x2="20" y1="12" y2="12"/><line x1="4" x2="20" y1="6" y2="6"/><line x1="4" x2="20" y1="18" y2="18"/></svg>
            <svg v-else xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18 6 6 18"/><path d="m6 6 12 12"/></svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Navigation -->
    <div v-show="isMobileMenuOpen" class="md:hidden glass absolute top-full left-0 w-full border-t border-slate-200 py-4 px-4 flex flex-col gap-4 shadow-xl">
      <a v-for="link in navLinks" :key="link.name" :href="link.href" @click="isMobileMenuOpen = false" class="text-base font-semibold text-slate-700 hover:text-black px-4 py-2 rounded-lg hover:bg-slate-100 transition-colors">
        {{ link.name }}
      </a>
      <a href="#contact" @click="isMobileMenuOpen = false" class="mt-2 text-center px-5 py-3 rounded-xl bg-black text-white font-medium shadow-md">
        Get a Quote
      </a>
    </div>
  </header>
</template>
