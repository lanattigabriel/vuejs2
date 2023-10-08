<template>
  <div class="posts">
    <img src="../assets/img/FB-Logo.svg" alt="page logo" class="logo" />
    <CardComp
      class="mt-2 mx-auto single-post"
      image="https://images.pexels.com/photos/165505/pexels-photo-165505.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
      title="Sunset"
      :header="{ name: 'Joe Jones', img:'https://randomuser.me/api/portraits/men/51.jpg', desc:'user avatar'}"
      :likes="true"
    />
    <CardComp
      class="mt-2 mx-auto single-post"
      image="https://images.pexels.com/photos/1738964/pexels-photo-1738964.jpeg?auto=compress&cs=tinysrgb&w=600"
      title="I love winter"
      :header="{ name: 'Susan Smith', img:'https://randomuser.me/api/portraits/women/4.jpg', desc:'user avatar'}"
    />
  </div>
</template>

<script>
import CardComp from "../components/CardComp.vue";
export default {
  name: "PostsView",
  components: {
    CardComp
  },
};
</script>

<style scoped>
.posts {
  min-height: 60vh;
  max-width: 895px;
  margin: auto;
}

.logo {
  max-width: 200px;
  padding: 2rem;
}

.single-post {
  max-width: 550px;
}
</style>
