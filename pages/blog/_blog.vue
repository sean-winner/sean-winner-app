<template lang="html">
  <div class="mt-6 mb-6 lg:mt-10 border-b border-gray-400">
    <article>
      <div class="markdown mt-4 max-w-xl" v-html="$md.render(blogPost.body)" />
    </article>
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
