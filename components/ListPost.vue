<template>
  <div>
    <ul v-if="posts">
      <Post
        v-for="post in posts"
        :id="post.id"
        :key="post.id"
        :title="post.title"
      />
    </ul>
  </div>
</template>

<script>
import Post from './Post.vue'
export default {
  components: { Post },
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
}
</script>
