<script setup lang="ts">
const props = defineProps({
  createdAt: {
    type: String,
    required: true,
  },
})

const postedDate = computed(() => {
  const date = new Date(props.createdAt)
  return date.toLocaleDateString('ja-JP')
})
</script>

<template>
  <time class="block text-sm text-gray-500">{{ postedDate }}</time>
</template>
