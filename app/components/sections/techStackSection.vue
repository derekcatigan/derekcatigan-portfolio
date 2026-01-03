<script setup>
const techStacks = [
  {
    category: "Frontend & Libraries",
    stacks: [
      "HTML",
      "CSS",
      "JavaScript",
      "JQuery",
      "Vue.js",
      "InertiaJs",
      "Nuxt.js",
      "Tailwind CSS",
      "Bootstrap",
      "DaisyUI",
      "Vite",
    ],
  },
  {
    category: "Backend & Databases",
    stacks: ["PHP", "Laravel", "MySQL", "PostgreSQL", "Node.js", "C#"],
  },
  {
    category: "Development Tools",
    stacks: [
      "VS Code",
      "Xampp",
      "MySQL Workbench",
      "Git",
      "GitHub",
      "Figma",
      "Affinity",
      "QGIS",
    ],
  },
];
</script>

<template>
  <section class="p-10 mx-auto">
    <!-- Section Header -->
    <div class="text-center mb-14">
      <i class="bx bx-medical-flask text-3xl text-blue-500"></i>
      <h2 class="text-2xl text-blue-500 font-bold mt-2">MY TECH STACKS</h2>
      <p class="text-gray-500 text-sm mt-1">
        Technologies and tools I use to build reliable, scalable, and
        user-focused web applications.
      </p>
    </div>

    <div class="mx-auto max-w-7xl">
      <!-- Tech Category -->
      <div
        data-aos="fade-up"
        v-for="(tech, index) in techStacks"
        :key="index"
        class="mb-5">
        <p class="font-bold text-gray-700">{{ tech.category }}</p>

        <div class="w-full grid grid-cols-2 lg:grid-cols-3 gap-3 mt-2">
          <div
            v-for="(stack, i) in tech.stacks"
            :key="i"
            class="p-2 text-center text-sm bg-white border border-gray-300 rounded shadow truncate">
            <span>{{ stack }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
