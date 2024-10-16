<template>
  <div>
    <div class="container">
      <div class="doc-body row">
        <div class="doc-content col-md-9 col-12 order-1">
          <div class="content-inner">
            <section id="code-section" class="doc-section">
              <div id="html" class="section-block">
                <div class="code-block">
                  <pre>
                        <i class="fa-regular fa-copy"></i>
                        <code class="language-markup">&lt;!DOCTYPE html&gt; 
                          &lt;html lang=&quot;en&quot;&gt; 
                              ...
                              &lt;div class=&quot;jumbotron&quot;&gt; 
                                  &lt;h1&gt;Hello, world!&lt;/h1&gt; 
                                  &lt;p&gt;...&lt;/p&gt; 
                                  &lt;p&gt;&lt;a class=&quot;btn btn-primary btn-lg&quot; href=&quot;#&quot; role=&quot;button&quot;&gt;Learn more&lt;/a&gt;&lt;/p&gt; 
                              &lt;/div&gt;
                              &lt;div class=&quot;jumbotron&quot;&gt; 
                                  &lt;h1&gt;Hello, world!&lt;/h1&gt; 
                                  &lt;p&gt;...&lt;/p&gt; 
                                  &lt;p&gt;&lt;a class=&quot;btn btn-primary btn-lg&quot; href=&quot;#&quot; role=&quot;button&quot;&gt;Learn more&lt;/a&gt;&lt;/p&gt; 
                              &lt;/div&gt;
                              ...
                          &lt;/html&gt; 
                        </code>
                  </pre>
                </div>
              </div>
            </section>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
import from ''
<script>
import "../assets/css/styles.css";
import "../assets/plugins/simplelightbox/simple-lightbox.min.css";
import "../assets/plugins/elegant_font/css/style.css";
import "../assets/plugins/prism/prism.css";
import "../assets/plugins/bootstrap/css/bootstrap.min.css";

export default {
  name: "CodeBlock"
};
</script>

<style>
/* Add your styles here */
</style>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
.language-markup {
  width: 100% !important;
}
.language-css {
  width: 100% !important;
}
.language-python {
  width: 100% !important;
}
</style>
