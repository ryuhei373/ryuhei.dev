<script setup lang="ts"></script>

<template>
  <header class="container mx-auto flex flex-col flex-wrap items-center pb-12 text-gray-600 md:flex-row">
    <nuxt-link
      to="/"
      class="mb-4 flex items-center font-medium text-yellow-500 hover:text-yellow-600 md:mb-0"
    >
      <img
        src="https://github.com/ryuhei373.png"
        width="32"
        height="32"
        alt="ryuhei373"
        class="mr-3 inline-block rounded-full"
      >
      <span class="text-xl font-bold">ryuhei.dev</span>
    </nuxt-link>
    <!-- <nav class="flex flex-wrap items-center justify-center text-base md:ml-auto">
      <nuxt-link to="about" class="mr-5 hover:text-gray-900">
        About
      </nuxt-link>
      <nuxt-link to="portfolio" class="hover:text-gray-900">
        Portfolio
      </nuxt-link>
    </nav> -->
  </header>
</template>
