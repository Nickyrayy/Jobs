<template>
  <div>
    <TheHeader />
    <main class="container mx-auto p-6">
      <slot />
    </main>
    </div>
</template>

<script setup>
import TheHeader from '~/components/TheHeader.vue';
</script>