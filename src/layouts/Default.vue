<template>
  <div class="max-w-2xl m-auto">
    <header class="flex justify-between items-center mb-5 h-14">
      <strong>
        <g-link to="/">{{ $static.metadata.siteName }}</g-link>
      </strong>
      <nav class="">
        <g-link class="ml-5" to="/">Home</g-link>
        <g-link class="ml-5" to="/about/">About</g-link>
      </nav>
    </header>
    <slot/>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>
