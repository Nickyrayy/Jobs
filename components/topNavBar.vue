<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'

const items = ref<NavigationMenuItem[][]>([
  [
    {
        label: 'My Internship',
        to: '/jobs',
        class: 'text-bold'
    },
    {
        label: 'Job Search',
        icon: 'i-lucide-briefcase',
        to: '/jobs',
    },
    {
        label: 'Dashboard',
        icon: 'i-lucide-grid',
        to: '/userDashboard',
    }
  ]
])

</script>

<template>
    <div class="flex-row">
        <UNavigationMenu 
            orientation="horizontal" 
            :items="items" 
            class="
            w-full
            " 
        />

        <div class="flex-1" />

    </div>
</template>