<template>
  <ul class="list-group">
    <li class="list-group-item text-muted">10 Likes</li>
    <li class="list-group-item">
      <div class="row">
        <div class="col d-grid px-0">
          <button class="btn d-flex justify-content-center align-items-center">
            <span class="material-icons-outlined"> thumb_up </span>
            Like
          </button>
        </div>
        <div class="col d-grid px-0">
          <button class="btn d-flex justify-content-center align-items-center">
            <span class="material-icons-outlined"> comment </span>
            Comment
          </button>
        </div>
      </div>
    </li>
  </ul>
</template>

<script>
export default {};
</script>

<style scoped>
    .btn:hover {
        color: #5044c9;
    }
</style>