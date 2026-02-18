<script setup>
import { ref } from 'vue'

const categories = [
  { name: "Kadhannaa", slug: "kadhannaa" },
  { name: "Jaalala", slug: "jaalala" },
  { name: "Amantaa", slug: "amantaa" },
  { name: "Of Bituu", slug: "of-bituu" },
  { name: "Sooma", slug: "sooma" },
  { name: "Hiriyyaa Gaarii", slug: "hiriyyaa-gaarii" },
  { name: "Qulqullummaa", slug: "qulqullummaa" },
  { name: "Abdii", slug: "abdii" },
  { name: "Of Eeggannaa", slug: "of-eeggannaa" },
  { name: "Waa'ee Dubroo Maariyaam", slug: "waaee-dubroo-maariyaam" },
  { name: "Gorsa", slug: "gorsa" },
  { name: "Obsa", slug: "obsa" },
  { name: "Gaabbii", slug: "gaabbii" }
]


const selectedCategory = ref(null)

const selectCategory = (cat) => {
  selectedCategory.value = cat
}
</script>

<template>
  <div
    class="relative min-h-screen bg-cover bg-center flex flex-col justify-center items-center text-white 
           pt-24 sm:pt-28 md:pt-32 lg:pt-36"
    style="background-image: url('/images/spiritual-bg.jpg')"
  >

    <div class="absolute inset-0 bg-black/60 "></div>

    <div class="relative z-10 text-center px-6 max-w-4xl">
      
      <h1 class="text-4xl md:text-6xl font-bold leading-tight mb-6 animate-fadeIn">
        Spiritual Quotes
      </h1>

      <p class="text-lg md:text-xl text-gray-200 mb-10">
        Inspirational Wisdom from Faith Fathers ✨  
        Strengthen Your Spirit. Guide Your Life.
      </p>

      <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-4">
        <div
          v-for="cat in categories"
          :key="cat.slug"
          @click="selectCategory(cat)"
          class="cursor-pointer bg-white/10 hover:bg-white/20 backdrop-blur-md border border-white/20 rounded-xl py-3 px-4 text-sm md:text-base transition-all duration-300 hover:scale-105"
        >
          <NuxtLink :to="`/${cat.slug}`" class="block w-full h-full">
            {{ cat.name }}
          </NuxtLink>
        </div>
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
