<template>
  <div class="detail">
    详情页
    <div class="hljs" ref="hlDiv" v-html="blogDetail"></div>
  </div>
</template>

<script>
import marked from 'marked';
import hljs from 'highlight.js';
import 'highlight.js/styles/monokai-sublime.css';
export default {
  components: {},
  props: {},
  data() {
    return {
      blogDetail: '```javascript\nfunction(){\n\tconsole.log(123)\n}\n```',
    };
  },
  computed: {},
  methods: {},
  created() {},
  mounted() {
    marked.setOptions({
      renderer: new marked.Renderer(),
      highlight: function(code) {
        return hljs.highlightAuto(code).value;
      },
      pedantic: false,
      gfm: true,
      tables: true,
      breaks: false,
      sanitize: false,
      smartLists: true,
      smartypants: false,
      xhtml: false,
    });
    this.blogDetail = marked(this.blogDetail);
  },
};
</script>
<style lang="less" scoped>
.common-box {
  padding: 0 20px;
  border-radius: 6px;
  background-color: #fff;
  box-shadow: 0 6px 10px 0 rgb(20 36 70 / 8%);
}
.detail {
  .common-box();
  padding: 20px;
}
</style>
