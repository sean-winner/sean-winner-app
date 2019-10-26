<template lang="html">
  <div>
    <h3 class="text-gray-900 sm:text-lg lg:text-xl">
      <a href="#" class="hover:underline">{{ title }}</a>
    </h3>
    <div
      class="flex text-gray-700 text-sm sm:text-base lg:text-lg mt-2 sm:mt-3 lg:mt-3"
    >
      {{ description }}
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Cool thing'
    },
    description: {
      type: String,
      default: 'A really cool description of a really cool project. 🤯'
    }
  }
}
</script>
