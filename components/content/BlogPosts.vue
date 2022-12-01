<script setup lang="ts">
import PostedDate from '../PostedDate.vue'

const { data } = await useAsyncData(() => {
  return queryContent('/blog/').find()
})
</script>

<template>
  <article v-for="post in data" :key="post._id" class="pb-4">
    <NuxtLink
      :to="post._path"
    >
      <h1 class="text-2xl font-bold tracking-wide hover:text-yellow-600">
        {{ post.title }}
      </h1>
    </NuxtLink>
    <PostedDate class="mb-6" :created-at="post.createdAt" />
    <p class="leading-loose">
      {{ post.description }}
    </p>
    <NuxtLink
      :to="post._path"
      class="
            mt-4
            flex
            items-center
            justify-end
            gap-2
            text-yellow-500
            hover:text-yellow-600
          "
    >
      <span>Read more</span>
      <svg
        class="h-4 w-4"
        viewBox="0 0 24 24"
        stroke="currentColor"
        stroke-width="2"
        fill="none"
        stroke-linecap="round"
        stroke-linejoin="round"
      >
        <path d="M5 12h14" />
        <path d="M12 5l7 7-7 7" />
      </svg>
    </NuxtLink>
  </article>
</template>
