<!-- app\pages\project.vue -->
<script setup>
import PinoyPrideWebsite from "@/assets/projects/PinoyPrideWebsite.png";
import PinoyPridePanel from "@/assets/projects/PinoyPridePanel.png";
import HavilahSystem from "@/assets/projects/HavilahSystem.png";
import FirstAidSystem from "@/assets/projects/FirstAidSystem.png";
import MswdSystem from "@/assets/projects/MswdSystem.png";

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
  // {
  //   projectImage: HavilahSystem,
  //   projectTitle: "Havilah Polymedic Online Appointment with Queueing System",
  //   projectDescription: `
  //       A web-based appointment and queueing system developed for a medical clinic to streamline patient scheduling and reduce waiting time.
  //       The system enables patients to book appointments online while allowing staff to manage queues, appointments, and service flow efficiently.
  //       `,
  //   techStack: ["PHP", "Laravel", "JQuery", "MySQL", "TailwindCSS", "DaisyUI"],
  // },
  // {
  //   projectImage: FirstAidSystem,
  //   projectTitle: "First Aid Vendo Management System",
  //   projectDescription: `
  //       A management system built to monitor and manage first aid vending machines.
  //       The system tracks inventory, machine status, and item availability, helping administrators ensure timely restocking and efficient operation.
  //       `,
  //   techStack: ["PHP", "Laravel", "JQuery", "MySQL", "TailwindCSS", "DaisyUI"],
  // },
  {
    projectImage: MswdSystem,
    projectTitle: "MSWD Management Information System",
    projectDescription: `
        A web-based management system developed for the Municipality MSWD to digitize and streamline their manual document and service records. 
        The system helps staff manage MSWD services, track documents efficiently, and improve workflow. 
        I implemented a map visualization feature to support data-driven decision making for community programs. 
        Throughout the project, I collaborated with my team on development, testing, and documentation, ensuring a functional and user-friendly solution.
        `,
    techStack: [
      "PHP",
      "Laravel",
      "JQuery",
      "MySQL",
      "HTML",
      "CSS",
      "Bootstrap",
      "Leaflet",
    ],
  },
];

useSeoMeta({
  title: "Projects – Derek Joshua Catigan",
  ogTitle: "Projects – Derek Joshua Catigan",
  description:
    "Portfolio of web applications and projects by Derek Joshua Catigan, showcasing real-world problem solving, clean design, and scalable systems.",
  ogDescription:
    "Explore projects by Derek Joshua Catigan, including web applications and systems that showcase real-world problem solving, clean design, and scalability.",
  keywords:
    "Derek Joshua Catigan, Web Developer, Full Stack Developer, PHP, Laravel, Vue.js, Inertia.js, Web Applications, Portfolio, Freelance Developer, Capstone Projects",
});
</script>

<template>
  <section class="p-5 mx-auto">
    <!-- Section Header -->
    <div class="text-center mb-14">
      <i class="bx bx-grid-column-right text-3xl text-blue-500"></i>
      <h2 class="text-2xl text-blue-500 font-bold mt-2">PROJECTS</h2>
      <p class="text-gray-500 text-sm mt-1">
        Explore projects that solve real problems with clean design, responsive
        layouts, and efficient web solutions.
      </p>
    </div>

    <!-- Back Button -->
    <NuxtLink to="/" class="btn btn-sm btn-neutral mb-3">
      <i class="bx bx-chevron-left"></i> Back
    </NuxtLink>

    <!-- Projects Grid -->
    <div class="flex flex-col gap-3">
      <!-- Projects Card -->
      <div
        v-for="(project, index) in projects"
        :key="index"
        data-aos="fade-up"
        class="p-3 bg-white border border-gray-300 shadow-md rounded">
        <div class="flex flex-wrap items-stretch gap-1">
          <!-- Project Image -->
          <div
            class="w-full md:w-72 lg:w-80 p-3 border border-gray-300 rounded shadow-lg overflow-hidden">
            <img
              :src="project.projectImage"
              alt="Project"
              class="w-full h-64 object-contain" />
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
  </section>
</template>
