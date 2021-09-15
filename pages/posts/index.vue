<template>
  <div>
    <NavBar />

    <h1>List post</h1>

    <p v-if="errors">{{ errors }}</p>

    <!-- lista de publicaciones -->
    <ListPost :posts="posts" />
  </div>
</template>

<script>
import axios from 'axios'
import ListPost from '../../components/ListPost.vue'
import NavBar from '../../components/NavBar.vue'

export default {
  components: {
    ListPost,
    NavBar,
  },
  data() {
    return {
      posts: [],
      errors: null,
    }
  },
  async created() {
    try {
      const { data } = await axios.get(
        'https://jsonplaceholder.typicode.com/posts'
      )
      this.posts = data
    } catch (error) {
      this.errors = error.message
    }
  },
}
</script>
