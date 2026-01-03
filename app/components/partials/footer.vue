<script setup>
const currentYear = new Date().getFullYear();
</script>
<template>
  <footer
    class="footer sm:footer-horizontal bg-neutral text-neutral-content p-5">
    <div class="w-full flex flex-col justify-center items-center">
      <i class="bx bx-terminal text-5xl"></i>
      <p class="text-center">
        Derek Joshua Catigan
        <br />
        <span class="flex items-center gap-1">
          <i class="bx bx-copyright"></i> {{ currentYear }} All rights reserved.
        </span>
      </p>
    </div>
  </footer>
</template>
