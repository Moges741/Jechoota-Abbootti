<script setup>
import QuoteCard from '../components/QuoteCard.vue'
import { kadhannaa } from '../components/Kadhannaa/kadhannaaQuotes.js'
</script>

<template>
  <div
    class="min-h-screen bg-cover bg-center flex items-center justify-center p-6"
    style="background-image: url('/images/spiritual-bg.jpg')"
  >
    <div class="absolute inset-0 bg-black/70 backdrop-blur-sm"></div>

    <div class="relative z-10 max-w-3xl w-full space-y-10">
      
      <QuoteCard
        v-for="item in kadhannaa"
        :key="item.id"
        :quote="item.quote"
        :author="item.author"
      />

    </div>
  </div>
</template>
