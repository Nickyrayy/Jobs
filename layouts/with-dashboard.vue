<script setup>
import dashboardNavBar from '~/components/dashboardNavBar.vue';
import topNavBar from '~/components/topNavBar.vue';
</script>

<template>
  <div class="flex max-h-screen">
    <dashboardNavBar />
    <topNavBar />
    <main class="flex-1 container mx-auto p-6">
      <slot />
    </main>
   </div>
</template>