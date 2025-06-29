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
        <UNavigationMenu 
            orientation="horizontal" 
            :items="items"
            variant="link" 
            class="
            w-full
            " />
</template>