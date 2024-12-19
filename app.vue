<template>
  <div class="flex flex-col h-screen w-full dark:bg-black overflow-hidden">
    <Topbar />
    <main class="flex-1 overflow-auto">
      <NuxtPage />
      <Footer />
    </main>
  </div>
</template>

<script setup>
import Topbar from "~/components/app/Topbar.vue";
import Footer from "~/components/app/Footer.vue";
</script>
