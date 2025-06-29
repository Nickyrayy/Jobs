<script setup>
import topNavBar from '~/components/topNavBar.vue';
</script>

<template>
  <div class="flex flex-col h-screen">
    <header class="shrink-0">
      <topNavBar />
    </header>
      <main class="flex-1 container overflow-y-auto p-6">
        <slot />
      </main>
  </div>
</template>