<!-- app\components\sections\projectSection.vue -->
<script setup>
import PinoyPrideWebsite from "@/assets/projects/PinoyPrideWebsite.png";
import PinoyPridePanel from "@/assets/projects/PinoyPridePanel.png";
import HavilahSystem from "@/assets/projects/HavilahSystem.png";
import FirstAidSystem from "@/assets/projects/FirstAidSystem.png";

const projects = [
  {
    projectImage: PinoyPrideWebsite,
    projectTitle: "Pinoy Pride Worldwide LLC Website",
    projectDescription: `
        A modern, user-friendly corporate website rebuilt from a legacy system to improve customer experience and accessibility.
        The project focuses on clean UI design, responsive layout, and clear content presentation, allowing customers to easily view company services and track their balikbayan boxes.
        `,
    techStack: [
      "PHP",
      "Laravel",
      "Inertia.js",
      "Vue.js",
      "TailwindCSS",
      "DaisyUI",
    ],
  },
  {
    projectImage: PinoyPridePanel,
    projectTitle: "Pinoy Pride Worldwide LLC Panel",
    projectDescription: `
        An internal web-based management panel designed to support logistics operations.
        The system allows administrators to manage orders, employees, and container tracking statuses, providing an organized and scalable solution for day-to-day operational workflows.
        `,
    techStack: [
      "PHP",
      "Laravel",
      "Inertia.js",
      "Vue.js",
      "MySQL",
      "TailwindCSS",
      "DaisyUI",
    ],
  },
  {
    projectImage: HavilahSystem,
    projectTitle: "Havilah Polymedic Online Appointment with Queueing System",
    projectDescription: `
        A web-based appointment and queueing system developed for a medical clinic to streamline patient scheduling and reduce waiting time.
        The system enables patients to book appointments online while allowing staff to manage queues, appointments, and service flow efficiently.
        `,
    techStack: ["PHP", "Laravel", "JQuery", "MySQL", "TailwindCSS", "DaisyUI"],
  },
  {
    projectImage: FirstAidSystem,
    projectTitle: "First Aid Vendo Management System",
    projectDescription: `
        A management system built to monitor and manage first aid vending machines.
        The system tracks inventory, machine status, and item availability, helping administrators ensure timely restocking and efficient operation.
        `,
    techStack: ["PHP", "Laravel", "JQuery", "MySQL", "TailwindCSS", "DaisyUI"],
  },
];
</script>

<template>
  <section class="p-10 mx-auto bg-blue-900">
    <!-- Section Header -->
    <div class="text-center mb-14">
      <i class="bx bx-grid-column-right text-3xl text-yellow-500"></i>
      <h2 class="text-2xl text-yellow-500 font-bold mt-2">PROJECTS</h2>
      <p class="text-gray-100 text-sm mt-1">
        A selection of projects showcasing real-world problem solving, clean
        design, and scalable web systems.
      </p>
    </div>

    <!-- Projects Grid -->
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-3">
      <!-- Projects Card -->
      <div
        v-for="(project, index) in projects"
        :key="index"
        data-aos="fade-up"
        class="p-3 bg-white border border-gray-300 shadow-md rounded">
        <div class="flex flex-wrap items-stretch gap-1">
          <!-- Project Sample -->
          <div
            class="flex-1 min-w-50 p-3 border border-gray-300 rounded shadow-lg overflow-hidden">
            <img
              :src="project.projectImage"
              alt="Project"
              class="w-full object-cover" />
          </div>

          <div class="flex-1 min-w-50 p-3">
            <div class="flex flex-col justify-between h-full gap-3">
              <div class="space-y-4">
                <!-- Project Title -->
                <h3 class="text-md font-bold text-gray-700">
                  {{ project.projectTitle }}
                </h3>

                <!-- Project Description -->
                <div class="leading-relaxed lg:text-justify text-sm">
                  <p>
                    {{ project.projectDescription }}
                  </p>
                </div>
              </div>

              <!-- Project Tech Stack -->
              <div class="flex flex-wrap justify-end gap-2">
                <span
                  v-for="(tech, techIndex) in project.techStack"
                  :key="techIndex"
                  class="badge badge-soft bg-blue-50 border border-blue-500 text-blue-700">
                  {{ tech }}
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="w-full flex justify-center items-center mt-5">
      <NuxtLink to="/project" class="btn btn-warning">
        <i class="bx bx-arrow-in-up-right-square"></i> See More
      </NuxtLink>
    </div>
  </section>
</template>
