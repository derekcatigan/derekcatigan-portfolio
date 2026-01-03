<!-- app\layouts\default.vue -->
<script setup>
import { onMounted } from "vue";
import AOS from "aos";
import "aos/dist/aos.css";

import Header from "~/components/partials/header.vue";
import Footer from "~/components/partials/footer.vue";

onMounted(() => {
  AOS.init({
    easing: "ease",
    once: false,
  });
});
</script>
<template>
  <Header />
  <!-- Main Content -->
  <main class="min-h-screen overflow-hidden bg-gray-100">
    <slot />
  </main>
  <Footer />
</template>
