<template>
  <div>
    <NavBar />
    <h1>About Us</h1>
    <p>
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolor
      perferendis atque, reprehenderit, quas esse odit ad at magnam possimus est
      libero a suscipit dolorum unde.
    </p>
  </div>
</template>

<script>
import NavBar from '../components/NavBar.vue'
export default {
  components: { NavBar },
  // CEO
  head() {
    return {
      title: 'Posts | Nuxt application',
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
