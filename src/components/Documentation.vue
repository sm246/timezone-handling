<template>
  <div>
    <div class="page-wrapper">
      <!-- ******Header****** -->
      <header id="header" class="header">
        <div class="container">
          <div class="branding">
            <h1 class="logo">
              <a href="index.html">
                <span aria-hidden="true" class="fas fa-clock"></span>
                <span class="text-highlight"> TimeZone </span
                ><span class="text-bold">Handling</span>
              </a>
            </h1>
          </div>
          <!--//branding-->

          <div class="top-search-box">
            <form
              @submit.prevent="performSearch"
              class="form-inline search-form justify-content-center"
            >
              <input
                type="text"
                v-model="searchQuery"
                placeholder="Search..."
                name="search"
                class="form-control search-input"
              />

              <button type="submit" class="btn search-btn" value="Search">
                <i class="fas fa-search"></i>
              </button>
            </form>
            <div v-if="results.length">
              <h3>Search Results:</h3>
              <ul>
                <li v-for="result in results" :key="result.id">
                  {{ result.name }}
                </li>
              </ul>
            </div>
          </div>
        </div>
        <!--//container-->
      </header>
      <!--//header-->
      <div class="doc-wrapper">
        <div class="container">
          <div id="doc-header" class="doc-header text-center">
            <h1 class="doc-title">
              <i class="icon fa fa-paper-plane"></i> Quick Start
            </h1>
          </div>
          <div class="doc-body row">
            <div class="doc-content col-md-9 col-12 order-1">
              <div class="content-inner">
                <introduction />
                <BrowserTimezone />
                <!-- <timezone
                  id="profile-timezone-section"
                  :isUseful="false"
                  title="Profile Timezone"
                /> -->
                <!-- <section id="profile-timezone-section" class="doc-section">
                  <h2 class="section-title">Profile Timezone</h2>
                  <div id="html" class="section-block">
                    <div class="code-block">
                      <h6>HTML Code Example</h6>
                      <code-block />
                    </div>
                  </div>
                </section> -->
                <!-- <section id="database-timezone-section" class="doc-section">
                  <h2 class="section-title">Database Timezone</h2>
                  <div id="html" class="section-block">
                    <div class="code-block">
                      <h6>HTML Code Example</h6>
                      <code-block />
                    </div>
                  </div>
                </section>
                <section id="background-timezone-section" class="doc-section">
                  <h2 class="section-title">Background Timezone</h2>
                  <div id="html" class="section-block">
                    <div class="code-block">
                      <h6>HTML Code Example</h6>
                      <code-block />
                    </div>
                  </div>
                </section> -->
              </div>
            </div>
            <div class="doc-sidebar col-md-3 col-12 order-0 d-none d-md-flex">
              <div id="doc-nav" class="doc-nav">
                <nav id="doc-menu" class="nav doc-menu flex-column sticky">
                  <li class="nav-item">
                    <a class="nav-link scrollto" href="#introduction-section"
                      >Introduction</a
                    >
                  </li>

                  <!--//nav-->
                  <li class="nav-item">
                    <a
                      class="nav-link scrollto"
                      href="#browser-timezone-section"
                    >
                      Browser’s Timezone</a
                    >
                  </li>

                  <li class="nav-item">
                    <a
                      class="nav-link scrollto"
                      href="#profile-timezone-section"
                    >
                      Profile Timezone</a
                    >
                  </li>
                  <!-- <nav class="nav doc-sub-menu nav flex-column">
                    <li class="nav-item">
                      <a class="nav-link scrollto" href="#html">HTML</a>
                    </li>
                    <li class="nav-item">
                      <a class="nav-link scrollto" href="#css">CSS</a>
                    </li>
                    <li class="nav-item">
                      <a class="nav-link scrollto" href="#sass">Sass</a>
                    </li>
                    <li class="nav-item">
                      <a class="nav-link scrollto" href="#less">LESS</a>
                    </li>
                  </nav> -->
                  <li class="nav-item">
                    <a
                      class="nav-link scrollto"
                      href="#database-timezone-section"
                    >
                      Database Timezone</a
                    >
                  </li>
                  <li class="nav-item">
                    <a
                      class="nav-link scrollto"
                      href="#background-timezone-section"
                    >
                      Background Timezone</a
                    >
                  </li>
                </nav>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import "../assets/css/styles.css";
import "../assets/plugins/simplelightbox/simple-lightbox.min.css";
import "../assets/plugins/elegant_font/css/style.css";
import "../assets/plugins/prism/prism.css";
import "../assets/plugins/bootstrap/css/bootstrap.min.css";
import Introduction from "./Introduction.vue";
import BrowserTimezone from "./BrowserTimezone.vue";

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Documentation",
  components: {
    Introduction,
    BrowserTimezone
  },
  data() {
    return {
      searchQuery: "",
      results: []
    };
  },
  methods: {
    performSearch() {
      // Simulate an API call
      const mockResults = [
        { id: 1, name: "Result 1" },
        { id: 2, name: "Result 2" },
        { id: 3, name: "Result 3" }
      ];

      // Filter results based on the search query
      this.results = mockResults.filter((result) =>
        result.name.toLowerCase().includes(this.searchQuery.toLowerCase())
      );
    }
  }
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
