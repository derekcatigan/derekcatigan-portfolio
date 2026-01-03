<script setup>
import PinoyPrideLogo from "@/assets/logos/PinoyPrideLogoOriginal.png";
import BizmatechLogo from "@/assets/logos/BizmatechLogo.png";
import SLSULOGO from "@/assets/logos/SLSULOGO.png";
import CatiganProfile from "@/assets/images/CatiganProfileNoBG.png";

const experiences = [
  {
    logo: PinoyPrideLogo,
    company: "Pinoy Pride Worldwide LLC",
    role: "Junior Software Developer",
    duration: "September 2025 - Present",
    description: `
           I rebuilt the company’s legacy website into a modern, clean, and user-friendly web application, improving both usability and overall customer experience. I implemented tracking features that allow customers to monitor the status of their balikbayan boxes in real time, increasing transparency and trust. In addition, I developed an internal web system to manage logistics orders, employee records, and container tracking with status updates. This role allowed me to work on real production systems while gaining hands-on experience in building scalable, reliable, and maintainable web applications.
        `,
  },
  {
    logo: CatiganProfile,
    company: "Freelance",
    role: "Software Developer",
    duration: "June 2025 - Present",
    description: `
           After graduating, I worked as a Freelance Software Developer, where I assisted clients and students in developing and improving their web-based systems and capstone projects. I collaborated closely with clients to understand their requirements, implemented features, fixed bugs, and optimized existing functionalities. This experience strengthened my problem-solving skills, adaptability, and ability to deliver practical solutions while managing time effectively and working independently.
        `,
  },
  {
    logo: BizmatechLogo,
    company: "Business Machine Technologies, Inc.",
    role: "Intern - Software Developer",
    duration: "January 2025 - April 2025",
    description: `
           During my internship at Business Machine Technologies, Inc., I assisted the development team in building a web-based system designed to manage customer invoices, products, and employee records. I supported backend development tasks by implementing CRUD operations, working with database interactions, and helping resolve real-world system requirements. This experience exposed me to collaborative development, practical problem-solving, and the importance of writing clean, maintainable code in a real business environment.
        `,
  },
  {
    logo: SLSULOGO,
    company: "Southern Leyte State University - Capstone Project",
    role: "Programmer - Role",
    duration: "November 2024 - January 2025",
    description: `
       For my capstone project, I collaborated with my team to develop a web-based system for the Municipality MSWD to digitize and manage their manual document records. 
       The system streamlined the management of MSWD services and documents, reducing manual workload and improving operational efficiency. 
       I implemented a map visualization feature to assist staff in decision-making and to better address community needs. 
       Throughout the project, I actively contributed to backend and frontend development, testing, and documentation, while coordinating tasks within my team to ensure smooth collaboration and timely delivery.
    `,
  },
];
</script>

<template>
  <section class="px-6 mx-auto py-5 bg-white">
    <!-- Section Header -->
    <div class="text-center mb-14">
      <i class="bx bx-briefcase-alt-2 text-3xl text-blue-500"></i>
      <h2 class="text-2xl text-blue-500 font-bold mt-2">EXPERIENCE</h2>
      <p class="text-gray-500 text-sm mt-1">
        Professional and Hands-on Development Experience
      </p>
    </div>

    <!-- Experience Grid -->
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-3">
      <div
        v-for="(experience, index) in experiences"
        :key="index"
        data-aos="fade-up"
        class="bg-white border border-gray-300 rounded-sm shadow-sm p-3 lg:p-6 flex flex-col">
        <!-- Header -->
        <div class="flex items-center gap-4 mb-4">
          <!-- Logo -->
          <img
            :src="experience.logo"
            alt="Company Logo"
            class="w-16 h-16 object-contain border border-gray-300 rounded-sm shadow-lg p-2 bg-gray-50" />

          <!-- Meta -->
          <div class="flex-1">
            <h3 class="text-md lg:text-lg font-semibold">
              {{ experience.company }}
            </h3>
            <p class="text-blue-600 font-medium">
              {{ experience.role }}
            </p>
            <p class="text-sm text-gray-500 italic">
              {{ experience.duration }}
            </p>
          </div>
        </div>

        <!-- Description -->
        <div
          class="text-gray-700 leading-relaxed text-left lg:text-justify flex-1">
          {{ experience.description }}
        </div>
      </div>
    </div>
  </section>
</template>
