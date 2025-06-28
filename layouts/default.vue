<script setup>
import navBar from '~/components/navBar.vue';
</script>

<template>
  <div class="flex max-h-screen">
    <navBar />
    <main class="flex-1 container mx-auto p-6">
      <slot />
    </main>
    </div>
</template>