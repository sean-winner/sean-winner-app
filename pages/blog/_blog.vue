<template lang="html">
  <div class="mt-6 lg:mt-10 border-b border-gray-400">
    <div class="lg:flex items-center justify-between">
      <article>
        <h3 class="text-gray-900 font-semibold text-xl">
          {{ blogPost.title }}
        </h3>
        <div class="mt-2">
          {{ blogPost.description }}
        </div>
        <div
          class="markdown mt-4 max-w-xl"
          v-html="$md.render(blogPost.body)"
        />
      </article>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ params, payload }) {
    if (payload) return { blogPost: payload }
    else
      return {
        blogPost: await require(`~/assets/content/blog/${params.blog}.json`)
      }
  }
}
</script>
