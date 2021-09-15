<template>
  <nuxt-link :to="`/posts/${id}`">
    <div class="post">
      <p>{{ id }}. {{ title }}</p>
    </div>
  </nuxt-link>
</template>

<script>
export default {
  name: 'Post',
  props: {
    id: {
      type: Number,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
  },
}
</script>

<style scoped>
.post {
  padding: 1rem;
  border: 1px solid whitesmoke;
  margin: 1rem 0;
}

.post:hover {
  background-color: rgb(226, 223, 223);
  border: 1px solid #9185e7;
  cursor: pointer;
}

a {
  color: black;
  text-decoration: none;
}

a:hover {
  color: #9185e7;
}
</style>
