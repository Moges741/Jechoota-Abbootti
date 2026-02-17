<script setup>
import { ref } from 'vue'

const categories = [
    "Kadhannaa",
    "Jaalala",
  "Amantaa",
  "Of Bituu",
  "Sooma",
  "Hiriyyaa Gaarii",
  "Qulqullummaa",
  "Abdii",
  "Of Eeggannaa",
  "Waa'ee Dubroo Maariyaam",
  "Gorsa",
  "Obsa",
  "Gaabbii"
]

const selectedCategory = ref(null)

const selectCategory = (cat) => {
  selectedCategory.value = cat
}
</script>

<template>
  <div
    class="relative min-h-screen bg-cover bg-center flex flex-col justify-center items-center text-white"
    style="background-image: url('/images/spiritual-bg.jpg')"
  >

    <div class="absolute inset-0 bg-black/60 "></div>

    <div class="relative z-10 text-center px-6 max-w-4xl">
      

      <h1 class="text-4xl md:text-6xl font-bold leading-tight mb-6 animate-fadeIn">
        Spiritual Quotes
      </h1>

      <!-- Subtitle -->
      <p class="text-lg md:text-xl text-gray-200 mb-10">
        Inspirational Wisdom from Faith Fathers ✨  
        Strengthen Your Spirit. Guide Your Life.
      </p>

      <!-- Categories Grid -->
      <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-4">
        <NuxtLink
          v-for="cat in categories"
          :key="cat"
          @click="selectCategory(cat)"
          :to="`/${cat.toLowerCase()}`"
          class="bg-white/10 hover:bg-white/20 backdrop-blur-md border border-white/20 rounded-xl py-3 px-4 text-sm md:text-base transition-all duration-300 hover:scale-105"
        >
          {{ cat }}
        </NuxtLink>
      </div>

    </div>
  </div>
</template>

<style>
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

.animate-fadeIn {
  animation: fadeIn 1s ease-out;
}
</style>
