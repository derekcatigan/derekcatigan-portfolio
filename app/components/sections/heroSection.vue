<script setup>
import CatiganProfile from "@/assets/images/CatiganProfile.jpg";
import Blob from "@/assets/images/BlobSample.png";
import Resume from "/assets/documents/Resume(Catigan).pdf";
</script>
<template>
  <div class="hero min-h-screen relative overflow-hidden">
    <img
      :src="Blob"
      alt="Blob background"
      class="absolute w-250 sm:w-100 md:w-125 lg:w-220 -top-24 sm:-top-40 md:-top-56 lg:-top-64 -right-24 sm:-right-40 md:-right-56 lg:-right-56 pointer-events-none" />
    <div class="hero-content flex-col lg:flex-row-reverse">
      <img
        data-aos="fade-left"
        :src="CatiganProfile"
        class="max-w-sm w-80 lg:w-96 rounded-md shadow-md" />
      <div data-aos="fade-right">
        <p class="font-medium text-gray-500">Hi, I am</p>
        <h1 class="text-3xl lg:text-5xl font-bold">
          DEREK JOSHUA
          <span class="text-blue-700">CATIGAN</span>
        </h1>
        <p class="text-blue-700">Software Developer</p>
        <p class="py-6">
          I specialize in building modern web applications with clean,
          user-friendly interfaces and minimalist design. I also work as a
          freelancer, developing efficient and scalable web systems.
        </p>
        <div class="flex flex-wrap items-center gap-2">
          <a :href="Resume" target="_blank" class="btn btn-primary">
            <i class="bx bx-archive-arrow-down"></i>
            Download CV
          </a>
          <a href="mailto:derekcatigan03@gmail.com" class="btn btn-neutral">
            <i class="bx bx-envelope-alt"></i>
            Send Email
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
