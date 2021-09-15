<template>
  <div>
    <p v-if="isLoading">Loading...</p>
    <p v-if="errors">Error" {{ errors }}</p>

    <div v-if="post">
      <h1>Detalle del producto {{ post.id }}</h1>
      <h1>{{ post.title }}</h1>
      <p>{{ post.body }}</p>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      post: {},
      errors: null,
      isLoading: false,
    }
  },
  async created() {
    const { id } = this.$route.params
    this.isLoading = true

    try {
      const { data } = await axios.get(
        `https://jsonplaceholder.typicode.com/posts/${id}`
      )
      this.post = data
    } catch (error) {
      this.errors = error.message
    }
    this.isLoading = false
  },
}
</script>
