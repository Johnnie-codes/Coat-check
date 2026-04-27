<script setup>
import { ShieldCheck, QrCode, Clock, Users, Smartphone, CreditCard } from 'lucide-vue-next';

const features = [
  {
    icon: QrCode,
    title: 'Digital Tickets',
    description: 'Guests receive a digital ticket via SMS or Apple/Google Wallet. No more lost paper stubs or forgotten items.'
  },
  {
    icon: Clock,
    title: 'Lightning Fast Retrieval',
    description: 'Our proprietary organization system cuts retrieval times down significantly for every guest, even at peak times.'
  },
  {
    icon: ShieldCheck,
    title: 'Secure & Insured',
    description: 'Every item checked is photographed, tracked, and fully insured. We take liability off your venues shoulders.'
  },
  {
    icon: Users,
    title: 'Professional Staff',
    description: 'Uniformed, background-checked, and highly trained professionals who provide a VIP experience from start to finish.'
  },
  {
    icon: Smartphone,
    title: 'Live Analytics Dashboard',
    description: 'Track how many items are checked, average wait times, and peak usage hours in real-time from any device.'
  },
  {
    icon: CreditCard,
    title: 'Cashless Tipping & Payment',
    description: 'Guests can pay and tip seamlessly via Apple Pay, Google Pay, or credit card right from their phones.'
  }
];
</script>

<template>
  <section id="features" class="py-24 relative bg-slate-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
      <div class="text-center max-w-3xl mx-auto mb-16">
        <h2 class="text-slate-500 font-bold tracking-widest uppercase text-xs mb-3">Premium Service</h2>
        <h3 class="text-3xl md:text-5xl font-black mb-6 text-black">Not your average coat check.</h3>
        <p class="text-slate-600 text-lg">
          We've completely reimagined the coat check experience using modern technology to eliminate lines, lost items, and friction.
        </p>
      </div>

      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div v-for="(feature, index) in features" :key="index" class="bg-white p-8 rounded-3xl hover:-translate-y-2 transition-all duration-300 group border border-slate-200 shadow-sm hover:shadow-xl hover:shadow-black/5">
          <div class="w-14 h-14 rounded-2xl bg-slate-100 flex items-center justify-center text-black mb-6 group-hover:scale-110 transition-transform duration-300 group-hover:bg-black group-hover:text-white">
            <component :is="feature.icon" class="w-7 h-7" />
          </div>
          <h4 class="text-xl font-bold text-black mb-3">{{ feature.title }}</h4>
          <p class="text-slate-600 leading-relaxed">{{ feature.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
