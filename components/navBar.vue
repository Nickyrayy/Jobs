<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'

const items = ref<NavigationMenuItem[][]>([
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
  ]
])
</script>

<template>
  <div class="flex flex-col h-screen p-0 border-r border-gray-200 dark:border-gray-800 w-48 bg-grey-700">
    <UButton
        icon="i-lucide-home"
        to="/home"
        variant="link"
        label="Job Website"
        class="
          justify-center
          text-base
          m-2
        "
      />

    <UInput
      icon="i-lucide-search" 
      placeholder="Search..." 
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
    data-[orientation=vertical]:w-48 
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
      "
    />

  </div>
</template>
