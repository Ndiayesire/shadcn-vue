<script setup lang="ts">
import Banner from "~/components/app/Banner.vue";
import Card from "~/components/app/compo/Card.vue";
import Payment from "~/components/app/compo/Payment.vue";
import Issue from "~/components/app/compo/Issue.vue";
import Notif from "~/components/app/compo/Notif.vue";

useHead({
  title: "Shadcn-vue",
});
</script>

<template>
  <div class="flex flex-col min-h-screen items-center justify-center dark:bg-black p-4">
    <!-- Banner Section -->
    <Banner />

    <div class="relative p-8 w-full flex justify-center items-center">
      <!-- Carousel Container -->
      <div
        class="grid grid-cols-1 sm:grid-cols-1 gap-6 md:grid-cols-3 lg:grid-cols-4 w-full h-full"
      >
        <!-- Carousel Items -->
        <div class="flex-shrink-0 w-full">
          <Card />
        </div>
        <div class="flex-shrink-0 w-full">
          <Payment />
        </div>
        <div class="flex-shrink-0 w-full">
          <Issue />
        </div>
        <div class="flex-shrink-0 w-full">
          <Notif />
        </div>
      </div>
    </div>
  </div>
</template>
