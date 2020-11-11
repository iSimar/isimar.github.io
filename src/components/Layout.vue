<template>
  <div class="container">
    <div class="left">
      <Menu :onClickMenuLink="onClickMenuLink"></Menu>
    </div>
    <div class="right">
      <Post v-if="view === 'posts'" ></Post>
      <WorkLog v-if="view === 'worklog'" ></WorkLog>
    </div>
  </div>
</template>

<script>
import Menu from './Menu.vue'
import Post from './Post.vue'
import WorkLog from './WorkLog.vue'

export default {
  data: function () {
    return {
      view: 'posts'
    }
  },
  methods: {
    onClickMenuLink(view) {
      this.view = view
    }
  },
  components: {
    Menu,
    Post,
    WorkLog
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
    /* flex-direction: row; */
  }
  .container {
    flex-direction: column;
  }
}

.container .right {
  flex: 1;
}

</style>
