<script setup>
import Footer from '~/components/common/Footer.vue';
import NavBar from '~/components/common/NavBar.vue';



</script>

<template>
    <div>
      <NavBar />
        <slot />
        <Footer />
    </div>
</template>