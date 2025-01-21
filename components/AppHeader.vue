<template>
  <header class="flex flex-row flex-wrap sm:flex-nowrap items-center">
    <a href="#main-content" class="skip-to-content">Skip to content</a>
    <div class="font-sans font-medium text-lg text-nowrap pr-4">
      Nuxt Evolution
    </div>
    <UHorizontalNavigation
      class="border-b border-gray-200 dark:border-gray-800"
      :links="links"
    />
    <ColorModePicker />
  </header>
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
