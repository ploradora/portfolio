<template>
  <Nav />
  <header>
    <div class="component">
      <Hero />
    </div>
  </header>
  <main class="mains">
    <div class="component">
      <Work />
    </div>
    <div class="component">
      <About />
    </div>
    <div class="component">
      <Contact />
    </div>
  </main>
</template>

<script>
import Nav from "./components/Nav.vue";
import Hero from "./components/Hero.vue";
import Work from "./components/Work.vue";
import About from "./components/About.vue";
import Contact from "./components/Contact.vue";

export default {
  components: {
    Hero,
    Nav,
    Work,
    About,
    Contact,
  },
  data() {
    return {
      currentSection: "",
    };
  },
  mounted() {
   
  },
};
</script>

<style scoped lang="scss">
@import "./assets/globalStyles.scss";

header {
  height: 100vh;
  @include mobile-end {
    margin-left: auto;
    width: calc(100% - 72px);
  }
  @include desktop-large {
    margin: unset;
    margin: auto;
    width: 100%;
    max-width: 1700px;
  }
}
main {
  @include mobile-end {
    margin-left: auto;
    width: calc(100% - 72px);
  }
  @include desktop-large {
    margin: auto;
    width: 100%;
    max-width: 1700px;
  }
}
</style>
