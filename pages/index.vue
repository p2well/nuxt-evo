<template>
  <main id="main-content">
    <UContainer>
      <UCard class="mt-10" role="region" aria-labelledby="page-title">
        <template #header>
          <div class="flex justify-between">
            <h1 id="page-title">🧬 Nuxt Evolution</h1>
            <ColorScheme
              ><USelect
                v-model="$colorMode.preference"
                :options="['system', 'light', 'dark']"
                aria-label="Color Scheme Selector"
            /></ColorScheme>
          </div>
        </template>
      </UCard>
    </UContainer>
  </main>
</template>
