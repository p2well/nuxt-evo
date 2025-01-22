<template>
  <div class="font-sans font-medium text-lg text-nowrap pr-4">
    Nuxt Evolution
  </div>
  <UHorizontalNavigation
    class="border-b border-gray-200 dark:border-gray-800"
    :links="links"
  />
  <ColorModePicker />
</template>

<script setup lang="ts">
const links = [
  [
    {
      label: 'Home',
      icon: 'i-material-symbols-home-outline',
      to: '/',
    },
    {
      label: 'Users',
      icon: 'i-material-symbols-group-outline',
      to: '/users',
    },
    {
      label: 'About',
      icon: 'i-material-symbols-info-outline',
      to: '/about',
    },
  ],
];
</script>
