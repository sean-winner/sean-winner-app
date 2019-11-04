<template lang="html">
  <div>
    <h3 class="text-gray-900 sm:text-lg lg:text-xl">
      <nuxt-link :to="link" class="hover:underline">{{ title }}</nuxt-link>
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
    },
    link: {
      type: String,
      default: '#'
    }
  }
}
</script>
