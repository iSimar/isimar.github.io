<template>
  <div class="container">
    <h1 class="title">Lorem Ipsum is not simply random text</h1>
    <div class="metadata">
      <span class="date">
        <timeago :since="timestamp" :auto-update="10"></timeago>
      </span>
    </div>
    <div class="markdown-container">
     <vue-markdown :source="markdown"></vue-markdown>
    </div>
  </div>
</template>

<script>
import VueMarkdown from 'vue-markdown'

export default {
  components: {
    VueMarkdown
  },
  data () {
    return {
      timestamp: new Date(),
      markdown: `
### Getting Started
Lorem Ipsum is simply **dummy text of the printing** and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

<img src="http://gulfinfotech.com/wp-content/uploads/revslider/rev_slider_example/placeholder-blue.png" width="100%" />

### More Information

Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the undoubtable source. Lorem Ipsum comes from sections 1.10.32 and 1.10.33 of "de Finibus Bonorum et Malorum" (The Extremes of Good and Evil) by Cicero, written in 45 BC. This book is a treatise on the theory of ethics, very popular during the Renaissance. The first line of Lorem Ipsum, "Lorem ipsum dolor sit amet..", comes from a line in section 1.10.32.

The standard chunk of Lorem Ipsum used since the 1500s is reproduced below for those interested. Sections 1.10.32 and 1.10.33 from "de Finibus Bonorum et Malorum" by Cicero are also reproduced in their exact original form, accompanied by English versions from the 1914 translation by H. Rackham.

### Last Step

Nullam orci lacus, auctor eget maximus ac, eleifend suscipit mi. Vivamus id sagittis ipsum. In a ex mattis velit ultricies bibendum. Ut vel sodales turpis, eget dapibus lorem. Integer ut condimentum orci. Nulla luctus leo eget orci aliquet, non hendrerit justo vulputate. Proin ipsum nisi, tincidunt a tortor in, semper euismod nisl. Maecenas nisl nunc, finibus non risus ut, fermentum accumsan arcu. Sed posuere mi vitae augue consectetur, vitae rhoncus libero lobortis. Quisque sed metus metus. Morbi sit amet felis odio. Nullam posuere nisl a purus dapibus convallis. Duis tincidunt erat in sagittis iaculis. Duis lacus ex, tempus sit amet lectus sit amet, sollicitudin porttitor eros. Quisque ullamcorper sollicitudin urna nec suscipit.

\`\`\` javascript
var foo = function (bar) {
  return bar++;
};

console.log(foo(5));
\`\`\`

Nam eu velit ac quam sollicitudin malesuada nec a nisi. Vestibulum gravida leo in odio vehicula maximus. Donec nisl mauris, sollicitudin sit amet massa ac, efficitur dapibus mauris. Aenean aliquet diam quis turpis dapibus, facilisis pellentesque est ullamcorper. Sed efficitur imperdiet justo ac porta. Suspendisse nec eros nec urna molestie molestie. Donec dictum dui sed nulla blandit gravida. In hac habitasse platea dictumst. Ut iaculis sapien vitae magna congue, nec egestas mi ullamcorper. Maecenas viverra eu ligula ac posuere. Quisque neque magna, venenatis non nisl eu, suscipit condimentum lacus. Sed in est eget dui gravida consequat sed in arcu. In vitae est justo. Nullam viverra viverra mi aliquam iaculis.
      `
    }
   }
}
</script>

<style scoped>
  .container {
  	display: flex;
    flex-direction: column;
    padding-right: 30px;
    padding-top: 20px;
    overflow-y: scroll;
  }
  @media (max-width: 2024px) {
    .container {
      padding-right: 50%;
    }
  }
  @media (max-width: 1624px) {
    .container {
      padding-right: 30%;
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
  .title {
    border-bottom: 1px solid #ddd;
    margin-bottom: 5px;
  }
  .metadata {
    font-size: 12px;
    color: gray;
  }
  .markdown-container {
    padding-top: 12px;
  }
</style>