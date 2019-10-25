<template>
  <div>
    <div class="flex justify-between items-center mt-10">
      <h1
        class="text-lg sm:text-xl md:text-2xl lg:text-3xl text-gray-900 font-medium md:font-normal leading-none"
      >
        <nuxt-link to="/">Sean Winner</nuxt-link>
      </h1>
      <div class="block lg:hidden">
        <button type="button" @click="isOpen = !isOpen">
          <svg
            width="24"
            hieght="24"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              v-if="!isOpen"
              d="M2 6H22V7H2V6ZM2 12H22V13H2V12ZM22 18H2V19H22V18Z"
              class="fill-current text-gray-900"
            ></path>
            <path
              v-if="isOpen"
              d="M4 4L20 20M20 4L4 20"
              class=""
              stroke="#1A202C"
            ></path>
          </svg>
        </button>
      </div>
    </div>

    <div :class="isOpen ? 'block' : 'hidden'" class="lg:block">
      <div
        class="w-full block lg:flex lg:justify-between lg:border-b lg:border-gray-400 mt-10 text-gray-700 font-medium lg:text-lg"
      >
        <div class="lg:flex -mb-px">
          <nuxt-link
            to="/projects"
            class="block pb-6 border-b border-transparent lg:mt-0
    lg:mr-8 hover:text-gray-900"
            >Projects</nuxt-link
          >
          <nuxt-link
            to="/blog"
            class="block pb-6 border-b border-transparent lg:mt-0
    lg:mr-8 hover:text-gray-900"
            >Blog</nuxt-link
          >
        </div>
        <div class="lg:flex">
          <a
            href="https://twitter.com/sean_winner93"
            class="block lg:mt-0 lg:ml-8 flex align-center hover:text-gray-900"
          >
            <div>
              Twitter
            </div>
            <svg
              width="25"
              height="25"
              viewBox="0 0 25 25"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
              class="ml-1 -mt-px"
            >
              <path d="M16.5 13V18.5H6.5V8.5H12" stroke="#4A5568" />
              <path d="M10 15L18.5 6.5" stroke="#4A5568" />
              <path d="M14 6.5H18.5V11" stroke="#4A5568" />
            </svg>
          </a>
          <a
            href="https://www.instagram.com/sean.winner/?hl=en"
            class="block mt-6 lg:mt-0 lg:ml-8 flex align-center hover:text-gray-900"
          >
            <div>
              Instagram
            </div>
            <svg
              width="25"
              height="25"
              viewBox="0 0 25 25"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
              class="ml-1 -mt-px"
            >
              <path d="M16.5 13V18.5H6.5V8.5H12" stroke="#4A5568" />
              <path d="M10 15L18.5 6.5" stroke="#4A5568" />
              <path d="M14 6.5H18.5V11" stroke="#4A5568" />
            </svg>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    }
  }
}
</script>
