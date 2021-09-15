<template>
  <div>
    <NavBar />

    <h1>HOME PAGE</h1>
  </div>
</template>

<script>
import NavBar from '../components/NavBar.vue'
export default {
  components: { NavBar },
  // CEO
  head() {
    return {
      title: 'Application Nuxt posts | Home',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Website about posts',
        },
      ],
      htmlAttrs: {
        lang: 'en',
      },
    }
  },
}
</script>
