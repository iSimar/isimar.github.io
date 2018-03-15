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
  width: 200px;
  padding-top: 30px;
  padding-left: 10px;
  padding-right: 10px;
}
@media (max-width: 728px) {
  .container .left {
    display: none;
  }
}

.container .right {
  flex: 1;
  padding-left: 30px;
}

</style>
