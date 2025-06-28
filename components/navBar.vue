<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'

const items = ref<NavigationMenuItem[][]>([
  [
    {
      label: 'Job Website',
      icon: 'i-lucide-home',
      to: '/home'
    },
    {
      label: 'Applications',
      icon: 'i-lucide-file-text',
      to: '/applications'
    }
  ],
  [
    {
      label: 'My Jobs',
      icon: 'i-lucide-book-open',
      to: '/userJobs',
      children: [
        {
          label: 'Job 1',
          description: 'Job 1',
          to: '/userJobs/1'
        },
        {
          label: 'Job 2',
          description: 'Job 2',
          to: '/userJobs/2'
        },
        {
          label: 'Job 3',
          description: 'Job 3',
          to: '/userJobs/3'
        },
      ]
    },
    {
      label: 'Calendar',
      icon: 'i-lucide-calendar',
      to: '/calendar'
    }
  ],
  [
    {
      label: 'GitHub',
      icon: 'i-simple-icons-github',
      to: 'https://github.com/Nickyrayy/Jobs',
      target: '_blank'
    },
    {
      label: 'Help',
      icon: 'i-lucide-circle-help',
      disabled: true
    }
  ],
  [
    {
      label: 'Profile',
      icon: 'i-lucide-user',
      to: '/profile'
    },
    {
      label: 'Settings',
      icon: 'i-lucide-settings',
      to: '/settings'
    },
    {
      label: 'Logout',
      icon: 'i-lucide-log-out',
      to: '/logout'
    }
  ]
])
</script>

<template>
  <UNavigationMenu 
  orientation="vertical" 
  :items="items" 
  class="data-[orientation=vertical]:w-48 h-screen" />
</template>
