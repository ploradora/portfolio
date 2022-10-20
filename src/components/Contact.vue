<template>
  <footer id="contact">
    <p class="section-name-contact">Contact</p>
    <!-- <span class="material-symbols-outlined">expand_less</span> -->
    <div class="content">
      <div class="contact-info">
        <div class="mail">
          <p class="email">suciu.seb@gmail.com</p>
          <a href="mailto:suciu.seb@gmail.com">
            <img class="envelope" src="../assets/images/envelope.jpg" alt=""
          /></a>
        </div>
        <div class="socials">
          <a
            class="social"
            target="_blank"
            href="https://www.linkedin.com/in/sebastian-suciu-b54b85206/"
            ><i class="fa-brands fa-linkedin"></i
          ></a>
          <a
            class="social"
            target="_blank"
            href="https://www.behance.net/gallery/108658421/MCMLXI"
            ><i class="fa-brands fa-behance"></i
          ></a>
          <a
            class="social"
            target="_blank"
            href="https://www.instagram.com/febabian/"
            ><i class="fa-brands fa-instagram"></i
          ></a>
          <a
            class="social"
            target="_blank"
            href="https://www.youtube.com/watch?v=Z9djQBHojzg&t=XmYs&ab_channel=Ploradora"
            ><i class="fa-brands fa-youtube"></i
          ></a>
          <a
            class="social"
            target="_blank"
            href="https://soundcloud.com/ploradora"
            ><i class="fa-brands fa-soundcloud"></i
          ></a>
        </div>
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
    gsap.to(".email", {
      scrollTrigger: {
        trigger: ".email",
        start: "20px 100%",
      },
      y: 0,
      scale: 1,
      delay: 1,
      opacity: 1,
    });
    gsap.to(".envelope", {
      scrollTrigger: {
        trigger: ".envelope",
        start: "20px 100%",
      },
      opacity: 1,
    });
    gsap.to(".fa-brands", {
      scrollTrigger: {
        trigger: ".fa-brands",
        start: "15px 100%",
      },
      y: 0,
      opacity: 1,
      duration: 0.7,
      stagger: 0.1,
    });
  },
};
</script>

<style scoped lang="scss">
@import "../assets/globalStyles.scss";

footer {
  padding-top: 25px;
  padding-bottom: 20px;
  width: 100%;
  background-color: $footer-brown;
  > p {
    color: $header-color;
    font-size: 17px;
    font-weight: 500;
    text-align: end;
    padding-right: 5%;
    transform: translateX(30px);
    opacity: 0;
  }
  .content {
    margin: auto;
    width: 90%;
    .contact-info {
      padding-top: 40px;
      flex: 2;
      > p {
        opacity: 0;
        transform: translateX(-30px);
      }
      .socials {
        width: fit-content;
        margin: auto;
        a:first-child {
          padding-left: unset;
        }
        a {
          color: darken($main-color, 15%);
          padding: 5px;
          font-size: 26px;
          i {
            opacity: 0;
            transform: translateY(30px);
          }
          &:hover {
            color: $main-color;
            transition: all 0.15s ease-in-out;
          }
        }
      }
      .mail {
        margin-bottom: 30px;
        .email {
          text-align: center;
          margin-bottom: 20px;
          line-height: normal;
          font-weight: 500;
          font-size: 15px;
          transform: translateY(20px) scale(0.5);
          opacity: 0;
          color: darken($main-color, 15%);
        }
        img {
          opacity: 0;
          margin: auto;
          display: block;
          width: 120px;
          cursor: pointer;
          &:hover {
            box-shadow: 0 3px 10px 4px rgba(0, 0, 0, 0.14);
            transform: scale(1.1) rotate(6deg);
            transition: all 0.15s ease-in-out;
          }
        }
      }
    }
  }
  @include mobile-end {
    > p {
      padding-right: 10px;
    }
    .content {
      .contact-info {
        padding-top: 30px;
      }
    }
  }
  @include desktop-enter {
    .content {
      .contact-info {
        padding-top: 20px;
      }
    }
  }
  @include desktop-large {
  }
}
</style>
