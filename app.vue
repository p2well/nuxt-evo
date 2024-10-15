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
      label: 'Users',
      icon: 'i-heroicons-user-group',
      to: '/users',
    },
  ],
  [
    {
      label: 'About',
      icon: 'i-heroicons-information-circle',
      to: '/about'
    },
  ],
];
</script>
