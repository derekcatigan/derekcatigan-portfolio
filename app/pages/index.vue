<!-- app\pages\index.vue -->
<script setup>
import heroSection from "@/components/sections/heroSection.vue";
import experienceSection from "@/components/sections/experienceSection.vue";
import serviceSection from "@/components/sections/serviceSection.vue";
import projectSection from "@/components/sections/projectSection.vue";
import techStackSection from "@/components/sections/techStackSection.vue";
import contactSection from "@/components/sections/contactSection.vue";

useSeoMeta({
  title: "Derek Joshua Catigan – Full Stack Web Developer",
  ogTitle: "Derek Joshua Catigan – Full Stack Web Developer",
  description:
    "Derek Joshua Catigan – Full Stack Web Developer specializing in PHP, Laravel, Inertia.js, and Vue.js. Showcasing projects, services, and tech skills.",
  ogDescription:
    "Derek Joshua Catigan – Full Stack Web Developer specializing in PHP, Laravel, Inertia.js, and Vue.js. Showcasing projects, services, and tech skills.",
  keywords:
    "Derek Joshua Catigan, Web Developer, Full Stack Developer, PHP, Laravel, Vue.js, Inertia.js, Web Applications, Portfolio, Freelance Developer, Capstone Projects",
});
</script>
<template>
  <!-- Hero Section -->
  <section>
    <heroSection />
  </section>

  <!-- Experience Section -->
  <section>
    <experienceSection />
  </section>

  <!-- Services Section -->
  <section>
    <serviceSection />
  </section>

  <!-- Projects Section -->
  <section>
    <projectSection />
  </section>

  <!-- Tech Stack Section -->
  <section>
    <techStackSection />
  </section>

  <!-- Contact Section -->
  <section>
    <contactSection />
  </section>
</template>
