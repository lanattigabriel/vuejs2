<template>
  <div class="card">
    <CardHeader v-if="header" :header='header'/>
    <div class="card-body">
      <h5 class="card-title">{{ title }}</h5>
      <p v-if="text" class="card-text">
        {{ text }}
      </p>
      <img v-if="image" :src="image" alt="post-image" class="post-img"/>
      <ListGroup v-if="likes"/>
      <slot name="default"></slot>
      <div class="d-grid gap-2">
        <button
          v-for="btn in btns"
          :key="btn.txt"
          class="btn"
          :class="btn.class"
        >
          {{ btn.txt }}
        </button>
        <slot name="footer"></slot>
      </div>
    </div>
  </div>
</template>

<script>
import CardHeader from '@/components/CardHeader.vue';
import ListGroup from './ListGroup.vue';
export default {
  name: "CardComp",
  components: { CardHeader, ListGroup },
  props: ["title", "text", "btns", "image", "header", "likes"],
};
</script>

<style scoped>
.card {
  border: none;
  box-shadow: 0 2px 4px rgb(0 0 0 / 10%), 0 8px 16px rgb(0 0 0 / 10%);
}
.post-img {
  max-width: 100%;
}
</style>