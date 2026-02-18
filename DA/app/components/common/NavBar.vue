<template>
  <div>
    <nav class="fixed top-0 left-0 w-full z-50 bg-gray-900/50 backdrop-blur-lg p-4">
      <div class="container mx-auto flex items-center justify-between">
        
        <div class="text-yellow-500 text-lg font-bold">
          Jechoota Abbootti
        </div>

        <div>
          <NuxtLink to="/" class="text-gray-300 hover:text-white px-3 py-2 rounded-md text-sm font-medium transition">
            Home
          </NuxtLink>

          <NuxtLink to="/amantaa" class="text-gray-300 hover:text-white px-3 py-2 rounded-md text-sm font-medium transition">
            About
          </NuxtLink>

          <NuxtLink to="/contact" class="text-gray-300 hover:text-white px-3 py-2 rounded-md text-sm font-medium transition">
            Contact
          </NuxtLink>
        </div>

      </div>
    </nav>
  </div>
</template>
