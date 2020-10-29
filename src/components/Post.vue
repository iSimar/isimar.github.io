<template>
  <div class="container">
    <div class="title" v-if="pastInitalDelay">
      <h1 v-if="post.title">{{post.title}}</h1>
      <vue-content-loading v-else-if="pastInitalDelay"
        :height="loader.title.height"
        :primary="loader.title.primary"
        :secondary="loader.title.secondary">
        <rect x="0" y="16" rx="4" ry="4" width="100%" height="18" />
      </vue-content-loading>
    </div>
    <div class="metadata">
      <!-- <span class="date">
        <timeago v-if="post.date" :since="post.date" :auto-update="10"></timeago>
        <vue-content-loading v-else-if="pastInitalDelay"
        :height="loader.date.height"
        :primary="loader.date.primary"
        :secondary="loader.date.secondary">
          <rect x="0" y="0" rx="4" ry="4" width="60" height="8" />
        </vue-content-loading>
      </span> -->
    </div>
    <div class="markdown-container">
      <vue-markdown v-if="post.content" :source="post.content"></vue-markdown>
      <vue-content-loading v-else-if="pastInitalDelay"
        :height="loader.content.height"
        :primary="loader.content.primary"
        :secondary="loader.content.secondary">
          <rect x="0" y="10" rx="4" ry="4" width="100" height="12" />
          <rect x="0" y="37" rx="4" ry="4" width="97%" height="9" />
          <rect x="0" y="50" rx="4" ry="4" width="100%" height="9" />
          <rect x="0" y="63" rx="4" ry="4" width="99%" height="9" />
          <rect x="0" y="76" rx="4" ry="4" width="96%" height="9" />
          <rect x="0" y="89" rx="4" ry="4" width="80%" height="9" />
      </vue-content-loading>
    </div> 
  </div>
</template>

<script>
import VueMarkdown from 'vue-markdown'
import VueContentLoading from 'vue-content-loading'

export default {
  components: {
    VueMarkdown,
    VueContentLoading
  },
  data () {
    return {
	  pastInitalDelay: false,
      loader: {
        title: {
          height: 34.5,
          primary: '#5b7187',
          secondary: '#425d79'
        },
        date: {
          height: 9,
          primary: '#b7b7b7',
          secondary: 'gray'
        },
        content: {
          height: 100,
          primary: '#5b7187',
          secondary: '#425d79'
        }
      },
      post: {}
    }
   },
   mounted () {
    setTimeout(() => {
      this.$set(this, 'pastInitalDelay', true);
    }, 1000);
    var title = "First Post";
    fetch(`https://raw.githubusercontent.com/iSimar/Posts/master/${title.toLowerCase().replace(" ", "_")}.md`)
    .then((res) => {
      res.text()
      .then((text) => {
        this.$set(this, 'pastInitalDelay', true);
        this.$set(this, 'post', {
          title: title,
          date: new Date(),
          content: text
        })
      })
    })
  }
}
</script>

<style scoped>
  .container {
  	display: flex;
    flex-direction: column;
    padding-left: 30px;
    padding-right: 30px;
    padding-top: 20px;
    overflow-y: scroll;
	padding-bottom: 100px;
  }
  @media (max-width: 2024px) {
    .container {
      padding-right: 50%;
    }
  }
  @media (max-width: 1624px) {
    .container {
      padding-right: 40%;
    }
  }
  @media (max-width: 1324px) {
    .container {
      padding-right: 25%;
    }
  }
  @media (max-width: 1024px) {
    .container {
      padding-right: 20%;
    }
  }
  @media (max-width: 964px) {
    .container {
      padding-right: 30px;
    }
  }
  @media (max-width: 724px) {
    .container {
      overflow-y: visible;
      padding-left: 15px;
      padding-right: 15px;
      padding-top: 0px;
    }
  }
  .title {
    border-bottom: 1px solid #ddd;
    margin-bottom: 5px;
  }
  .title h1 {
    margin-bottom: 0px;
  }
  .metadata {
    font-size: 12px;
    color: gray;
  }
  .markdown-container {
    padding-top: 12px;
  }
</style>