<template>
  <section id="browser-timezone-section" class="doc-section">
    <h2 class="section-title">Browser’s Timezone</h2>
    <div class="section-block">
      <p>
        <a href="https://prismjs.com/" target="_blank">PrismJS</a>
        is used as the syntax highlighter here. You can
        <a href="https://prismjs.com/download.html" target="_blank"
          >build your own version</a
        >
        via their website should you need to.
      </p>
    </div>
    <div :id="id" class="section-block">
      <div class="callout-block callout-success" v-if="isUseful">
        <div class="icon-holder">
          <i class="fas fa-thumbs-up"></i>
        </div>
        <div class="content">
          <h4 class="callout-title">Useful Tip:</h4>
          <p>
            You can use this online
            <a href="https://mothereff.in/html-entities" target="_blank"
              >HTML entity encoder/decoder</a
            >
            to generate your code examples.
          </p>
        </div>
      </div>
      <div class="code-block">
        <h6>HTML Code Example</h6>
        <code-block />
      </div>
    </div>
  </section>
</template>
<script>
import "../assets/css/styles.css";
import "../assets/plugins/simplelightbox/simple-lightbox.min.css";
import "../assets/plugins/elegant_font/css/style.css";
import "../assets/plugins/prism/prism.css";
import "../assets/plugins/bootstrap/css/bootstrap.min.css";
import CodeBlock from "./CodeBlock.vue";

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "BrowserTimezone",
  props: ["id", "isUseful", "title"],
  components: {
    CodeBlock
  },
  data() {
    return {};
  }
};
</script>
