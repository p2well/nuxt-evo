<template>
  <a href="#main-content" class="skip-to-content">Skip to content</a>
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

<style scoped>
.skip-to-content {
  position: absolute;
  top: -40px;
  left: 0;
  background: #000;
  color: #fff;
  padding: 8px;
  z-index: 100;
}

.skip-to-content:focus {
  top: 0;
}
</style>
