<script setup>
const steps = [
  {
    title: 'Guest Arrives',
    description: 'Guest hands over their coat. Our staff quickly scans a unique QR code hanger and snaps a photo of the item.'
  },
  {
    title: 'Digital Ticket Sent',
    description: 'Guest scans a counter QR code or provides their phone number to instantly receive their digital ticket.'
  },
  {
    title: 'Enjoy the Event',
    description: 'Guest enjoys the party without worrying about a paper stub. They can request retrieval from their phone shortly before leaving.'
  },
  {
    title: 'Swift Departure',
    description: 'Guest shows their digital ticket screen. Staff hands them their coat in seconds. Guest can leave a cashless tip.'
  }
];
</script>

<template>
  <section id="how-it-works" class="py-24 bg-white border-y border-slate-200 relative overflow-hidden">
    <!-- Decorative background line -->
    <div class="absolute top-1/2 left-0 w-full h-px bg-gradient-to-r from-transparent via-slate-200 to-transparent hidden lg:block"></div>

    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="text-3xl md:text-5xl font-black mb-4 text-black">How it works</h2>
        <p class="text-slate-600 text-lg max-w-2xl mx-auto">A seamless flow designed to keep your guests moving and happy.</p>
      </div>

      <div class="grid lg:grid-cols-4 gap-8">
        <div v-for="(step, index) in steps" :key="index" class="relative group">
          <div class="bg-white rounded-3xl p-8 h-full relative z-10 border border-slate-200 shadow-sm group-hover:border-black transition-colors duration-300">
            <div class="text-5xl font-black text-slate-100 mb-6 group-hover:text-black transition-colors duration-300">#</div>
            <h4 class="text-xl font-bold text-black mb-3">{{ step.title }}</h4>
            <p class="text-slate-600">{{ step.description }}</p>
          </div>
          <!-- Connector line for mobile -->
          <div v-if="index < steps.length - 1" class="absolute -bottom-8 left-1/2 w-px h-8 bg-slate-200 lg:hidden"></div>
        </div>
      </div>
    </div>
  </section>
</template>
