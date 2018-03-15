<template>
  <ul class="container">
    <li class="title">
      <h3>Simar's Blog</h3>
    </li>
    <li class="link">
      <a>
        Posts
      </a>
    </li>
    <li class="link">
      <a>
        GitHub
      </a>
    </li>
    <li class="link">
      <a>
        Twitter
      </a>
    </li>
  </ul>
</template>

<script>
export default {}
</script>

<style scoped>
  .container {
    list-style: none;
    flex-direction: column;
    padding-top: 60px;
  }
  .container .title h3{
    margin: 0;
  }
  .container .link{
    padding-top: 10px;
  }
</style>