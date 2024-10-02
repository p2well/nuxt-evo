<template>
  <UHorizontalNavigation
    :links="links"
    class="border-b border-gray-200 dark:border-gray-800"
  />
  <NuxtPage />
</template>

<script setup lang="ts">
const links = [
  [
    {
      label: 'Home',
      icon: 'i-heroicons-home',
      to: '/',
    },
    {
      label: 'Horizontal Navigation',
      icon: 'i-heroicons-chart-bar',
    },
    {
      label: 'Command Palette',
      icon: 'i-heroicons-command-line',
    },
  ],
  [
    {
      label: 'Examples',
      icon: 'i-heroicons-light-bulb',
    },
    {
      label: 'Help',
      icon: 'i-heroicons-question-mark-circle',
      to: '/about'
    },
  ],
];
</script>
