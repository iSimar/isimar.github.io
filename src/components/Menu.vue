<template>
  <ul class="container">
    <div class="header">
      <li class="title">
        <h3>Simar's Blog</h3>
      </li>
      <li class="image">
        <img src="https://avatars2.githubusercontent.com/u/5649414?s=460&u=3cf00d716bb7b6e1f1b2dacd7ecb74653442c19a&v=4"
            style="border-radius: 50%; margin-top: 20px; margin-bottom: 20px;"
            height="100px" />
      </li>
    </div>
    <div class="links">
      <li class="link">
        <a href="/">
          Blog Posts
        </a>
      </li>
      <li class="link">
        <a href="https://github.com/iSimar" target="_blank">
          GitHub
        </a>
      </li>
      <li class="link">
        <a href="https://twitter.com/simartweets" target="_blank">
          Twitter
        </a>
      </li>
      <li class="link">
        <a href="https://www.linkedin.com/in/singhsimarpreet" target="_blank">
          LinkedIn
        </a>
      </li>
      <li class="link">
        <a href="https://simarsingh.com/resume" target="_blank">
          Resume
        </a>
      </li>
      <li class="link thisApp">
        <a href="https://github.com/iSimar/isimar.github.io" target="_blank">
          This is a Vue.js app
        </a>
      </li>
    </div>
  </ul>
</template>

<script>
export default {}
</script>

<style scoped>
  .container {
    display: flex;
    list-style: none;
    flex-direction: column;
    padding-top: 80px;
    padding-left: 65px;
  }
  @media (max-width: 964px) {
    .container {
      padding-left: 60px;
    }
  }
  @media (max-width: 728px) {
    .container {
      padding-top: 10px;
      padding-left: 20px;
      margin-bottom: -2px;
    }
    .container .links {
      display: flex;
      flex-direction: row;
    }
    .container .links .link {
      padding-right: 15px;
    }
    .container .image,
    .container .thisApp {
      display: none;
    }
    .container .title {
      display: flex;
      flex: 1;
    }
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
    font-weight: bold;
  }
  .container .thisApp { 
    font-size: 12px; 
    margin-top: 80px;
  }
</style>