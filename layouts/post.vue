<script setup lang="ts">
import PostedDate from '~~/components/PostedDate.vue'

const { page } = useContent()
</script>

<template>
  <div class="container mx-auto max-w-screen-md p-4 md:px-0">
    <SiteHeader />
    <article>
      <h1 class="text-2xl font-bold tracking-wide">
        {{ page.title }}
      </h1>
      <PostedDate class="mb-6" :created-at="page.createdAt" />
      <slot />
    </article>
    <!-- <Footer /> -->
  </div>
</template>

<style>
html {
  font-family: "Helvetica Neue",
    Arial,
    "Hiragino Kaku Gothic ProN",
    "Hiragino Sans",
    Meiryo,
    sans-serif;
  font-size: 16px;
  word-spacing: calc(1rem / 16);
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
</style>
