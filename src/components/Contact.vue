<template>
  <footer id="contact">
    <p class="section-name-contact">Contact</p>
    <!-- <span class="material-symbols-outlined">expand_less</span> -->
    <div class="content">
      <div class="contact-info">
        <p>Email: suciu.seb@gmail.com</p>
        <div class="socials">
          <a
            target="_blank"
            href="https://www.linkedin.com/in/sebastian-suciu-b54b85206/"
            ><i class="fa-brands fa-linkedin"></i
          ></a>
          <a
            target="_blank"
            href="https://www.behance.net/gallery/108658421/MCMLXI"
            ><i class="fa-brands fa-behance"></i
          ></a>
          <a target="_blank" href="https://www.instagram.com/febabian/"
            ><i class="fa-brands fa-instagram"></i
          ></a>
          <a
            target="_blank"
            href="https://www.youtube.com/watch?v=Z9djQBHojzg&t=XmYs&ab_channel=Ploradora"
            ><i class="fa-brands fa-youtube"></i
          ></a>
          <a target="_blank" href="https://soundcloud.com/ploradora"
            ><i class="fa-brands fa-soundcloud"></i
          ></a>
        </div>
      </div>
      <div class="image-container"></div>
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
  padding-top: 10px;
  padding-bottom: 30px;
  width: 100%;
  > p {
    padding-right: 10px;
    color: $header-color;
    font-size: 17px;
    font-weight: 500;
    text-align: end;
    padding-right: 5%;
    transform: translateX(100px);
    opacity: 0;
  }
  .content {
    margin: auto;
    width: 90%;
    .contact-info {
      padding-top: 100px;
      p {
        line-height: normal;
        font-weight: 500;
        margin-bottom: 15px;
        font-size: 15px;
        color: darken($main-color, 15%);
      }
      .socials {
        a:first-child {
          padding-left: unset;
        }
        a {
          color: $main-color;
          padding: 5px;
          font-size: 26px;
          &:hover {
            color: darken($main-color, 10%);
          }
        }
      }
    }
  }
  @include mobile-end {
    // height: 100vh;
    > p {
      padding-right: 10px;
    }
    .content {
      width: calc(100% - 20px);
    }
  }
  @include desktop-large {
    > p {
      padding-top: 40px;
    }
  }
}
</style>
