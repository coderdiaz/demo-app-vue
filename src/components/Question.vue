<template>
  <div class="flex flex-col">
    <span class="inline-block w-full text-center mb-2">{{ title }}</span>
    <div class="flex space-x-4">
      <button v-for="(option, index) in options" :key="index" class="px-3 py-3 bg-gray-100 rounded">
        {{ option.name }}
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Question',
  props: {
    title: String,
    options: {
      type: Array,
      required: true,
    },
  }
}
</script>