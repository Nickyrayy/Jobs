<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'

const items = ref<NavigationMenuItem[][]>([
  [
    {
      label: 'My Applications',
      icon: 'i-lucide-briefcase',
      to: '/userApplications',
      children: [
        {
          label: 'Application 1',
          description: 'Application 1',
          to: '/userApplications/1'
        },
        {
          label: 'Application 2',
          description: 'Application 2',
          to: '/userApplications/2'
        },
        {
          label: 'Application 3',
          description: 'Application 3',
          to: '/userApplications/3'
        },
      ]
    },
    {
      label: 'Calendar',
      icon: 'i-lucide-calendar',
      to: '/calendar'
    }
  ]
])
</script>

<template>
  <div 
    class="
          fixed top-0 left-0 h-screen w-1/10 m-0
          flex flex-col  
          bg-secondary-500 dark:bg-secondary-800 text-primary shadow-2xl">
    <UButton
        icon="i-lucide-home"
        to="/userDashboard"
        variant="link"
        label="User Dashboard"
        class="
          justify-center
          text-base
          m-2
        "
      />

    <UInput
      icon="i-lucide-search" 
      placeholder="Search Applications..." 
      class="
        m-2
        mb-6
        rounded-full
      "
      />

    <UNavigationMenu 
    orientation="vertical" 
    :items="items" 
    class="
    data-[orientation=vertical]:
    w-full
    " 
    />

    <div class="flex-1" />

    <UButton
      label = 'GitHub'
      icon = 'i-simple-icons-github'
      to = 'https://github.com/Nickyrayy/Jobs'
      target = '_blank'
      class="
        m-4
        rounded-full
        shadow-lg
      "
    />

  </div>
</template>
