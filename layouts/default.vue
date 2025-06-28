<script setup>
import navBar from '~/components/navBar.vue';
</script>

<template>
  <div>
    <navBar />
    <main class="container mx-auto p-6">
      <slot />
    </main>
    </div>
</template>