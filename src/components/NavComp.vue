<template>
  <nav class="navbar navbar-expand-lg bg-primary">
    <div class="container justify-content-evenly">
      <router-link
        name=""
        to="/"
        class="nav-link active"
        aria-current="page"
      >
        <span class="material-icons-round"> home </span>
      </router-link>
      <router-link
        name="about"
        to="/about"
        class="nav-link"
      >
        <span class="material-icons-round"> info </span>
      </router-link>
      <router-link
        name="posts"
        to="/posts"
        class="nav-link"
      >
        <span class="material-icons-round"> featured_play_list </span>
      </router-link>
    </div>
  </nav>
</template>

<script>
export default {
  name: "NavComp",
};
</script>

<style scoped>
.material-icons-round {
  color: white;
  font-size: 1.4em;
  background-color: rgba(222, 206, 206, 0.16);
  padding: 0.3em;
  margin: 0.1em;
  border-radius: 50%;
}

</style>