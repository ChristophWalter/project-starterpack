<template>
  <div class="m-auto max-w-2xl h-full flex flex-col">
    <header class="flex justify-between items-center mb-5 h-14">
      <g-link class="font-light text-lg tracking-wide" to="/">{{
        $static.metadata.siteName
      }}</g-link>
      <nav>
        <g-link class="font-light ml-5" to="/">Home</g-link>
        <g-link class="font-light ml-5" to="/about/">About</g-link>
      </nav>
    </header>
    <div class="flex-grow">
      <slot />
    </div>
    <footer class="flex justify-between items-center h-14">
      <g-link class="font-light ml-auto text-red" to="/privacy/"
        >Privacy Statement</g-link
      >
      <g-link class="font-light ml-5" to="/imprint/">Imprint</g-link>
    </footer>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
html,
body {
  @apply h-full;
}
</style>
