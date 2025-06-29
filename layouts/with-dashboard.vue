<script setup>
import dashboardNavBar from '~/components/dashboardNavBar.vue';
import topNavBar from '~/components/topNavBar.vue';
</script>

<template>
  <div class="flex h-screen">
    <aside class="shrink-0">
      <dashboardNavBar />
    </aside>
    <div class="ml-48 flex flex-col flex-1 overflow-hidden">
      <header class="shrink-0">
        <topNavBar />
      </header>
      <main class="flex-1 container overflow-y-auto p-6">
        <slot />
      </main>
    </div>
  </div>
</template>