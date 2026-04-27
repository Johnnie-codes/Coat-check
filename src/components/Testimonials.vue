<script setup>
import { Star } from 'lucide-vue-next';

const testimonials = [
  {
    quote: "Coat Check+ completely transformed our annual gala. The line at the end of the night used to take a long time; this year, no one waited more than a few moments.",
    author: "Sarah Jenkins",
    role: "Event Director, Metro Events",
    rating: 5
  },
  {
    quote: "The digital tickets are a game changer. We didn't have a single lost item or confused guest all night. Very professional staff too.",
    author: "David Chen",
    role: "Venue Manager, The Grand Hall",
    rating: 5
  },
  {
    quote: "Worth every penny. The cashless tipping was loved by the staff, and the analytics dashboard let me see exactly when peak times were.",
    author: "Amanda Torres",
    role: "Corporate Event Planner",
    rating: 5
  }
];
</script>

<template>
  <section id="testimonials" class="py-24 relative bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="text-3xl md:text-5xl font-black mb-4 text-black">Trusted by top venues</h2>
        <p class="text-slate-600 text-lg">Don't just take our word for it.</p>
      </div>

      <div class="grid md:grid-cols-3 gap-8">
        <div v-for="(testimonial, index) in testimonials" :key="index" class="bg-slate-50 p-8 rounded-3xl border border-slate-200 flex flex-col hover:shadow-lg transition-shadow">
          <div class="flex gap-1 mb-6">
            <Star v-for="i in testimonial.rating" :key="i" class="w-5 h-5 fill-black text-black" />
          </div>
          <p class="text-slate-700 text-lg leading-relaxed flex-grow mb-8 font-medium">
            "{{ testimonial.quote }}"
          </p>
          <div class="flex items-center gap-4">
            <div class="w-12 h-12 rounded-full bg-black text-white flex items-center justify-center font-bold text-lg">
              {{ testimonial.author.charAt(0) }}
            </div>
            <div>
              <p class="text-black font-bold">{{ testimonial.author }}</p>
              <p class="text-sm text-slate-500">{{ testimonial.role }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
