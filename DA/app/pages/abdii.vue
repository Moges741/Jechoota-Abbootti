<script setup>
import { onMounted, ref } from 'vue'
import QuoteCard from '~/components/QuoteCard.vue'
import { abdii } from '~/components/Abdii/abdiiQuotes.js'

const visible = ref(false)

onMounted(() => {
  visible.value = true
})
</script>

<template>
  <div class="relative min-h-screen bg-gradient-to-br from-gray-900 via-gray-800 to-black py-24 px-6">


    <div class="absolute top-20 left-10 w-72 h-72 bg-yellow-400/10 rounded-full blur-3xl"></div>
    <div class="absolute bottom-20 right-10 w-72 h-72 bg-indigo-500/10 rounded-full blur-3xl"></div>

    <div class="relative z-10 max-w-4xl mx-auto">

      <div class="text-center mb-16">
        <h1 class="text-4xl md:text-5xl font-bold text-white tracking-tight">
          Abdii Quotes
        </h1>
        <p class="text-gray-400 mt-4">
          Words of Hope to Strengthen Your Spirit
        </p>
      </div>

 
      <div
        class="space-y-12 transition-all duration-1000"
        :class="visible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-10'"
      >
        <QuoteCard
          v-for="item in abdii"
          :key="item.id"
          :quote="item.quote"
          :author="item.author"
        />
      </div>

    </div>
  </div>
</template>
