<script setup>
</script>

<template>
  <div class="flex max-h-screen">
    <topNavBar />
    <div class="flex-row">
      <main class="flex-1 container mx-auto p-6">
        <slot />
      </main>
    </div>
  </div>
</template>