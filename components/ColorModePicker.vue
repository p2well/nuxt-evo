<template>
  <div class="flex flex-row items-center text-nowrap">
    <ColorScheme placeholder="..." tag="span">
      <UButton
        v-for="theme of ['system', 'light', 'dark']"
        :aria-label="theme + ' color mode'"
        class="ml-1"
        :key="theme"
        @click="$colorMode.preference = theme"
        :icon="iconName(theme)"
        :variant="
          !$colorMode.unknown && theme === $colorMode.preference
            ? 'solid'
            : 'outline'
        "
        size="sm"
      >
      </UButton>
    </ColorScheme>
  </div>
</template>

<script setup lang="ts">
function iconName(theme: string): string {
  switch (theme) {
    case 'system':
      return 'i-material-symbols-computer-outline';
    case 'dark':
      return 'i-material-symbols-nightlight-outline';
    default:
      return 'i-material-symbols-sunny-outline';
  }
}
</script>
