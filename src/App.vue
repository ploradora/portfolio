<template>
  <Nav />
  <header>
    <Hero />
  </header>
  <main>
    <Work />
    <About />
    <Contact />
  </main>
</template>

<script>
// import { gsap } from "gsap";

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
    return {};
  },
  methods: {
    // beforeEnterNav(el) {
    //   el.style.opacity = 0;
    //   el.style.transform = "translateY(-35px)";
    // },
    // enterNav(el, done) {
    //   gsap.to(el, {
    //     opacity: 1,
    //     duration: 1,
    //     y: 0,
    //     onComplete: done,
    //   });
    // },
  },
  computed: {},
  mounted() {},
};
</script>

<style scoped lang="scss">
@import "./assets/globalStyles.scss";

header {
  height: 100vh;
  @include mobile-end {
    margin-left: auto;
    width: calc(100% - 70px);
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
    width: calc(100% - 70px);
  }
  @include desktop-enter {
    margin-left: unset;
    margin: auto;
    // width: ;
  }
  @include desktop-large {
    
  }
}
</style>

<!-- <template>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {},
  computed: {},
  Mounted() {},
};
</script>

<style scoped lang="scss">
@import './assets/globalStyles.scss';
</style> -->
