<template>
  <div class="container mx-auto min-h-screen flex flex-col">
    <div role="region" aria-label="skip navigation">
      <a
        href="#main"
        class="sr-only focus:not-sr-only focus:absolute focus:top-0 focus:left-0 focus:bg-black focus:text-white focus:dark:bg-white focus:dark:text-black focus:border-4 focus:border-primary-500 focus:p-1"
      >
        Skip to main content
      </a>
    </div>
    <header
      id="header"
      class="flex flex-row flex-wrap sm:flex-nowrap items-center"
    >
      <AppHeader />
    </header>
    <main id="main" class="flex-grow">
      <NuxtPage />
    </main>
    <footer id="footer" class="text-center py-4">
      <AppFooter />
    </footer>
  </div>
</template>
