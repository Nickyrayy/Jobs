<script setup>
import dashboardNavBar from '~/components/dashboardNavBar.vue';
</script>

<template>
  <div class="flex max-h-screen">
    <dashboardNavBar />
    <main class="flex-1 container mx-auto p-6">
      <slot />
    </main>
    </div>
</template>