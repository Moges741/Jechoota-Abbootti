<script setup>
const contacts = [
  {
    role: "Developer",
    name: "Your Name Here",
    email: "developer@email.com",
    phone: "+251 9XXXXXXXX",
    description: "Frontend & Backend Developer of Spiritual Quotes Platform"
  },
  {
    role: "Quotes Provider",
    name: "Quotes Giver Name",
    email: "quotes@email.com",
    phone: "+251 9XXXXXXXX",
    description: "Spiritual Father & Source of the Inspirational Quotes"
  }
]
</script>

<template>
  <div
    class="relative min-h-screen bg-cover bg-center flex items-center justify-center text-white"
    style="background-image: url('/images/contact-bg.jpg')"
  >
    <!-- Overlay -->
    <div class="absolute inset-0 bg-black/70 backdrop-blur-sm"></div>

    <!-- Content -->
    <div class="relative z-10 w-full max-w-6xl px-6 py-20">
      
      <!-- Title -->
      <div class="text-center mb-16">
        <h1 class="text-4xl md:text-6xl font-bold mb-4">
          Contact Us
        </h1>
        <p class="text-gray-300 text-lg">
          Get in touch with the Developer and the Spiritual Quotes Provider
        </p>
      </div>

      <!-- Contact Cards -->
      <div class="grid md:grid-cols-2 gap-10">
        
        <div
          v-for="person in contacts"
          :key="person.role"
          class="bg-white/10 backdrop-blur-md border border-white/20 rounded-2xl p-8 shadow-xl hover:scale-105 transition duration-300"
        >
          <h2 class="text-2xl font-semibold mb-2 text-yellow-400">
            {{ person.role }}
          </h2>

          <h3 class="text-xl font-bold mb-4">
            {{ person.name }}
          </h3>

          <p class="text-gray-300 mb-6">
            {{ person.description }}
          </p>

          <div class="space-y-2 text-sm md:text-base">
            <p>
              📧 Email: 
              <a :href="`mailto:${person.email}`" class="underline hover:text-yellow-300">
                {{ person.email }}
              </a>
            </p>

            <p>
              📞 Phone:
              <a :href="`tel:${person.phone}`" class="underline hover:text-yellow-300">
                {{ person.phone }}
              </a>
            </p>
          </div>
        </div>

      </div>

    </div>
  </div>
  
</template>
