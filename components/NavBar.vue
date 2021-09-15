<template>
  <header>
    <h1>Posts App</h1>

    <nav>
      <ul>
        <li>
          <nuxt-link to="/">Home</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/posts">Posts</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/about">About</nuxt-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
header {
  background-color: #473e88;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #fff;
  border-bottom: 1px solid rgb(197, 194, 194);
  padding: 1rem;

  position: sticky;
  top: 0;
}

h1 {
  color: #fff;
  font-weight: bold;
}

header ul {
  display: flex;
  list-style: none;
  align-items: center;
  margin: 0;
}

header a {
  color: whitesmoke;
  padding: 0.3rem 1rem;
  margin: 0;
  text-decoration: none;
  text-transform: uppercase;
}

header a:hover {
  background-color: #9185e7;
  border-radius: 20px;
}

header a .active {
  background-color: #9185e7;
  border-radius: 20px;
}

a.nuxt-link-active {
  font-weight: bold;
}
/* exact link will show the primary color for only the exact matching link */
a.nuxt-link-exact-active {
  background-color: #9185e7;
  border-radius: 20px;
}
</style>
