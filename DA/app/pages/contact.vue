<script setup>
import { EnvelopeIcon, PhoneIcon, UserIcon } from '@heroicons/vue/24/outline'

const contacts = [
  {
    role: "Developer",
    name: "Moges Sisay",
    email: "mogesse741@gmail.com",
    phone: "+251924433166",
    description: "Software Engineering Student (MERN Stack Developer) and Creator of Jechoota Abbootti"
  },
  {
    role: "Quotes Provider",
    name: "Ayantu",
    email: "quotes@email.com",
    phone: "+251966500071",
    description: "Biomedical Engineering Student and Spiritual Quotes Contributor"
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

    <div class="relative z-10 w-full max-w-6xl px-6 py-20">

      <!-- Title -->
      <div class="text-center mb-20">
        <h1 class="text-4xl md:text-6xl font-bold tracking-tight">
          Contact
        </h1>
        <p class="text-gray-300 mt-4 text-lg">
          Connect with the minds behind Jechoota Abbootti
        </p>
      </div>

      <!-- Cards -->
      <div class="grid md:grid-cols-2 gap-12">

        <div
          v-for="person in contacts"
          :key="person.role"
          class="group relative bg-white/5 backdrop-blur-xl border border-white/10 rounded-3xl p-10 shadow-2xl transition-all duration-500 hover:bg-white/10 hover:scale-[1.03]"
        >

          <!-- Glow effect -->
          <div class="absolute inset-0 rounded-3xl bg-gradient-to-br from-white/5 to-white/0 opacity-0 group-hover:opacity-100 transition duration-500"></div>

          <div class="relative z-10">

            <!-- Role -->
            <p class="text-sm uppercase tracking-widest text-yellow-400 mb-3">
              {{ person.role }}
            </p>

            <!-- Name -->
            <div class="flex items-center gap-3 mb-6">
              <UserIcon class="w-6 h-6 text-gray-300" />
              <h2 class="text-2xl font-semibold">
                {{ person.name }}
              </h2>
            </div>

            <!-- Description -->
            <p class="text-gray-300 leading-relaxed mb-8">
              {{ person.description }}
            </p>

            <!-- Contact Info -->
            <div class="space-y-4">

              <a
                :href="`mailto:${person.email}`"
                class="flex items-center gap-3 text-gray-200 hover:text-yellow-400 transition duration-300"
              >
                <EnvelopeIcon class="w-5 h-5" />
                <span>{{ person.email }}</span>
              </a>

              <a
                :href="`tel:${person.phone}`"
                class="flex items-center gap-3 text-gray-200 hover:text-yellow-400 transition duration-300"
              >
                <PhoneIcon class="w-5 h-5" />
                <span>{{ person.phone }}</span>
              </a>

            </div>

          </div>
        </div>

      </div>

    </div>
  </div>
</template>
