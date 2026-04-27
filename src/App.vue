<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import Features from './components/Features.vue'
import HowItWorks from './components/HowItWorks.vue'
import Testimonials from './components/Testimonials.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="min-h-screen bg-white text-slate-900 selection:bg-black selection:text-white">
    <Navbar />
    
    <main>
      <Hero />
      <Features />
      <HowItWorks />
      <Testimonials />
      
      <!-- CTA Section -->
      <section id="contact" class="py-24 relative overflow-hidden bg-slate-50">
        <div class="absolute inset-0 bg-[url('https://grainy-gradients.vercel.app/noise.svg')] opacity-5 pointer-events-none mix-blend-multiply"></div>
        <div class="absolute right-0 bottom-0 w-96 h-96 bg-slate-200 rounded-full blur-[100px] pointer-events-none"></div>
        
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10 text-center">
          <h2 class="text-4xl md:text-5xl font-bold mb-6 text-black">Ready to upgrade your coat check?</h2>
          <p class="text-xl text-slate-600 mb-10 max-w-2xl mx-auto">
            Get in touch today to learn how we can bring our premium digital coat check experience to your next event or venue.
          </p>
          <form @submit.prevent class="bg-white p-8 rounded-3xl max-w-xl mx-auto border border-slate-200 shadow-xl shadow-slate-200/50">
            <div class="grid grid-cols-2 gap-4 mb-4">
              <input type="text" placeholder="First Name" class="w-full bg-slate-50 border border-slate-200 rounded-xl px-4 py-3 text-slate-900 focus:outline-none focus:border-black focus:ring-1 focus:ring-black transition-all">
              <input type="text" placeholder="Last Name" class="w-full bg-slate-50 border border-slate-200 rounded-xl px-4 py-3 text-slate-900 focus:outline-none focus:border-black focus:ring-1 focus:ring-black transition-all">
            </div>
            <div class="mb-4">
              <input type="email" placeholder="Email Address" class="w-full bg-slate-50 border border-slate-200 rounded-xl px-4 py-3 text-slate-900 focus:outline-none focus:border-black focus:ring-1 focus:ring-black transition-all">
            </div>
            <div class="mb-6">
              <select class="w-full bg-slate-50 border border-slate-200 rounded-xl px-4 py-3 text-slate-600 focus:outline-none focus:border-black focus:ring-1 focus:ring-black transition-all appearance-none">
                <option value="" disabled selected>Event Type</option>
                <option value="venue">Permanent Venue</option>
                <option value="corporate">Corporate Event</option>
                <option value="gala">Gala / Fundraiser</option>
                <option value="other">Other</option>
              </select>
            </div>
            <button type="submit" class="w-full bg-black hover:bg-slate-800 text-white font-bold py-4 rounded-xl transition-all hover:-translate-y-1 shadow-lg shadow-black/10">
              Get a Free Quote
            </button>
          </form>
        </div>
      </section>
    </main>

    <Footer />
  </div>
</template>

<style>
/* Any additional global component styles */
</style>
