<script setup>
import { ref, onMounted } from 'vue'
import QuoteCard from '~/components/QuoteCard.vue'
import { gorsa } from '~/components/Gorsa/gorsaQuotes.js'

const visible = ref(false)

onMounted(() => {
  visible.value = true
})
</script>

<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-950 via-gray-900 to-black py-24 px-6 relative overflow-hidden">

 
    <div class="absolute top-20 left-10 w-72 h-72 bg-blue-500/10 rounded-full blur-3xl"></div>
    <div class="absolute bottom-20 right-10 w-72 h-72 bg-emerald-500/10 rounded-full blur-3xl"></div>

    <div class="relative z-10 max-w-4xl mx-auto">

   
      <div class="text-center mb-16">
        <h1 class="text-4xl md:text-5xl font-bold text-white tracking-wide">
          Gorsa
        </h1>
        <p class="text-gray-400 mt-3">
          Spiritual Guidance and Life Wisdom
        </p>
      </div>

      
      <div
        class="space-y-12 transition-all duration-700"
        :class="visible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-10'"
      >
        <QuoteCard
          v-for="item in gorsa"
          :key="item.id"
          :quote="item.quote"
          :author="item.author"
        />
      </div>

    </div>
  </div>
</template>
