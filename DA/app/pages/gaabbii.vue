<script setup>
import { onMounted, ref } from 'vue'
import QuoteCard from '~/components/QuoteCard.vue'
import { gaabbii } from '~/components/Gaabbii/gaabbiiQuotes.js'

const visible = ref(false)

onMounted(() => {
  visible.value = true
})
</script>

<template>
  <div class="min-h-screen bg-gradient-to-br from-gray-950 via-slate-900 to-black py-24 px-6 relative overflow-hidden">

   
    <div class="absolute top-20 left-10 w-72 h-72 bg-indigo-500/10 rounded-full blur-3xl"></div>
    <div class="absolute bottom-20 right-10 w-72 h-72 bg-purple-500/10 rounded-full blur-3xl"></div>

    <div class="relative z-10 max-w-4xl mx-auto">


      <div class="text-center mb-16">
        <h1 class="text-4xl md:text-5xl font-bold text-white">
          Gaabbii Quotes
        </h1>
        <p class="text-gray-400 mt-3">
          Wisdom on Repentance and Spiritual Renewal
        </p>
      </div>

  
      <div
        class="space-y-12 transition-all duration-700"
        :class="visible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-10'"
      >
        <QuoteCard
          v-for="item in gaabbii"
          :key="item.id"
          :quote="item.quote"
          :author="item.author"
        />
      </div>

    </div>
  </div>
</template>
