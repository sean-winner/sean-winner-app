<template lang="html">
  <div class="mt-6 lg:mt-10 border-b border-gray-400">
    <div class="border-t border-gray-400 py-6 sm:py-8 lg:py-10">
      <div class="lg:flex items-center justify-between">
        <div>
          <h3 class="text-gray-900 sm:text-lg lg:text-xl">
            <a href="#" class="hover:underline">{{ blogPost.title }}</a>
          </h3>
          <div
            class="flex text-gray-700 text-sm sm:text-base lg:text-lg mt-2 sm:mt-3 lg:mt-3"
          >
            {{ blogPost.description }}
          </div>
        </div>
        <div
          class="flex flex-wrap text-gray-900 text-sm sm:text-base lg:text-lg mt-2 sm:mt-3 lg:mt-0"
        >
          <div class="lg:ml-8">
            <a href="#" class="flex items-center group hover:underline">
              <div class="relative w-6 h-6">
                <svg
                  viewBox="0 0 24 24"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                  class="absolute group-hover:opacity-0 w-6 h-6"
                >
                  <path d="M19.5 11V21.5H2.5V4.5H13" stroke="#1A202C" />
                  <path
                    d="M7.5 16.5L21.5 2.5"
                    stroke="#1A202C"
                    stroke-linecap="round"
                  />
                  <path d="M15 2.5H21.5V9" stroke="#1A202C" />
                </svg>
                <svg
                  viewBox="0 0 24 24"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                  class="absolute opacity-0 group-hover:opacity-100 w-6 h-6"
                >
                  <path
                    d="M7.5 16.5L21.5 2.5"
                    stroke="#1A202C"
                    stroke-linecap="round"
                  />
                  <path
                    d="M6.43934 15.4393C5.85355 16.0251 5.85355 16.9749 6.43934 17.5607C7.02512 18.1464 7.97487 18.1464 8.56066 17.5607L20 6.12132V22H2V4H17.8787L6.43934 15.4393Z"
                    stroke="#1A202C"
                    stroke-linecap="round"
                  />
                  <path d="M15 2.5H21.5V9" stroke="#1A202C" />
                </svg>
              </div>
              <div class="mt-px ml-2 lg:hidden">
                Check out this project
              </div>
            </a>
          </div>
        </div>
      </div>
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
