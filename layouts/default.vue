<template>
  <div class="antialiased">
    <div class="max-w-5xl mx-auto px-6 md:px-8">
      <nav-bar />
      <nuxt />
    </div>
  </div>
</template>

<script>
import NavBar from '~/components/NavBar.vue'
export default {
  components: {
    NavBar
  }
}
</script>
