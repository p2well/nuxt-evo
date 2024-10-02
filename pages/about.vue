<template>
  <UContainer>
    <UCard class="mt-10">
      <template #header>
        <div class="flex justify-between">
          <h1>About</h1>
        </div>
      </template>
      <UAccordion :items="items" />
    </UCard>
  </UContainer>
</template>

<script setup lang="ts">
const items = [
  {
    label: 'Getting Started',
    icon: 'i-heroicons-information-circle',
    content:
      'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.',
  },
  {
    label: 'Installation',
    icon: 'i-heroicons-arrow-down-tray',
    content:
      'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.',
  },
  {
    label: 'Theming',
    icon: 'i-heroicons-eye-dropper',
    content:
      'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.',
  },
  {
    label: 'Layouts',
    icon: 'i-heroicons-rectangle-group',
    content:
      'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.',
  },
  {
    label: 'Components',
    icon: 'i-heroicons-square-3-stack-3d',
    content:
      'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.',
  },
  {
    label: 'Utilities',
    icon: 'i-heroicons-wrench-screwdriver',
    content:
      'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.',
  },
];
</script>
