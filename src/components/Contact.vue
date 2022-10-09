<template>
  <footer id="contact">
    <p class="section-name-contact">Contact</p>
    <span class="material-symbols-outlined">expand_less</span>
    <div class="content">
      <div class="contact-info">
        
      </div>
      <div class="image-container">

      </div>
    </div>
  </footer>
</template>

<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

export default {
  mounted() {
    gsap.to(".section-name-contact", {
      scrollTrigger: {
        trigger: ".section-name-contact",
        start: "30px 90%",
      },
      x: 0,
      opacity: 1,
    });
  },
};
</script>

<style scoped lang="scss">
@import "../assets/globalStyles.scss";

footer {
  padding-top: 50px;
  width: 100%;
  height: 500px;
  > p {
    color: $header-color;
    font-size: 17px;
    font-weight: 500;
    text-align: end;
    padding-right: 5%;
    margin-top: 10px;
    transform: translateX(100px);
    opacity: 0;
  }
  > p {
    padding-right: 10px;
  }
}
</style>
