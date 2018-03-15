<template>
  <div class="container">
    <div class="left">
      <Menu></Menu>
    </div>
    <div class="right">
      <Post></Post>
    </div>
  </div>
</template>

<script>
import Menu from './Menu.vue'
import Post from './Post.vue'

export default {
  components: {
    Menu,
    Post
  }
}
</script>

<style scoped>

.container {
  display: flex;
  flex: 1;
}

.container .left,
.container .right {
  display: flex;
}

.container .left {
  min-width: 215px;
}
@media (max-width: 964px) {
  .container .left {
    min-width: 200px;
  }
}
@media (max-width: 728px) {
  .container .left {
    display: none;
  }
}

.container .right {
  flex: 1;
}

</style>
