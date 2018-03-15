<template>
  <ul class="container">
    <li class="title">
      <h3>Simar's Blog</h3>
    </li>
    <li class="link">
      <a href="/">
        Posts
      </a>
    </li>
    <li class="link">
      <a href="https://github.com/iSimar" target="_blank">
        GitHub
      </a>
    </li>
    <li class="link">
      <a href="https://twitter.com/isimar36" target="_blank">
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
  .container .title h3 {
    margin: 0;
  }
  .container .link {
    padding-top: 10px;
  }
  .container .link a{
    color: #42b983;
    text-decoration: none;
  }
</style>