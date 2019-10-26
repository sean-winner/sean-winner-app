<template>
  <div
    class="mb-20 md:flex mt-10 lg:mt-6 items-baseline md:border-t md:border-gray-400 md:pt-2 lg:border-t-0 lg:pt-0"
  >
    <div class="w-full md:w-1/3">
      <h2
        class="font-medium sm:font-normal text-xl sm:text-2xl md:text-3xl lg:text-4xl text-gray-900"
      >
        Blog
      </h2>
    </div>
    <div class="w-full md:w-2/3 mt-6">
      <div class="text-lg sm:text-xl lg:text-2xl text-gray-700">
        <p>Welcome to my blog</p>
        <p class="mt-6">Here is some stuff I'm interested in:</p>
      </div>
      <div class="mt-6 lg:mt-10 border-b border-gray-400">
        <div class="border-t border-gray-400 py-6 sm:py-8 lg:py-10">
          <div
            v-for="blogPost in blogPosts"
            :key="blogPost.slug"
            class="lg:flex items-center justify-between"
          >
            <list-item
              :title="blogPost.title"
              :description="blogPost.description"
              :slug="blogPost.slug"
            />
            <arrow-box-link
              link-description="Check out this post"
              :link="'blog/' + blogPost.slug"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ListItem from '~/components/ListItem.vue'
import ArrowBoxLink from '~/components/ArrowBoxLink.vue'
export default {
  components: {
    ListItem,
    ArrowBoxLink
  },
  computed: {
    blogPosts() {
      return this.$store.state.blogPosts
    }
  }
}
</script>
