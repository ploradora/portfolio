<template>
  <nav>
    <div class="links">
      <a href="#home"><button class="btns">Home</button></a>
      <a href="#work"><button class="btns">Work</button></a>
      <a href="#about"><button class="btns">About</button></a>
      <a href="#contact"><button class="btns">Contact</button></a>
    </div>
  </nav>
</template>

<script>
import { gsap } from "gsap";

export default {
  data() {
    return {
      currentWidth: "",
      navButtons: false,
      desktopAnimation: false,
    };
  },
  methods: {},
  computed: {},
  mounted() {
    const transitionNavButton = () => {
      let windowWidth = window.innerWidth;
      this.currentWidth = windowWidth;
      if (windowWidth >= 499) {
        this.navButtons = false;
        this.desktopAnimation = true;
      }
      if (windowWidth <= 500) {
        this.navButtons = true;
        this.desktopAnimation = false;
      }
    };
    window.addEventListener("resize", transitionNavButton);

    let mm = gsap.matchMedia();
    mm.add("(max-width: 498.4px)", () => {
      gsap.to(".btns", {
        y: 0,
        opacity: 1,
        duration: 1,
        stagger: 0.15,
      });
    });
    mm.add("(min-width: 499px)", () => {
      gsap.to(".btns", {
        x: 0,
        opacity: 1,
        duration: 1,
        stagger: 0.15,
      });
    });
    mm.add("(min-width: 1600px)", () => {
      gsap.to(".btns", {
        y: 0,
        opacity: 1,
        duration: 1,
        stagger: 0.15,
      });
    });
  },
};
</script>

<style scoped lang="scss">
@import "../assets/globalStyles.scss";

nav {
  z-index: 100;
  position: fixed;
  width: 100%;
  font-family: $ff;
  background-color: $main-background;
  &::after {
    position: absolute;
    content: "";
    left: 50%;
    transform: translateX(-50%);
    width: 90%;
    height: 1px;
    background-color: lighten($header-color, 20%);
  }
  .links {
    margin: auto;
    padding-top: 10px;
    width: 90%;
    max-width: 300px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    .btns {
      position: relative;
      border: unset;
      background-color: unset;
      font-family: $ff;
      font-size: 16px;
      padding: 5px 12px 15px 12px;
      opacity: 0;
      transform: translateY(-40px);
      color: $header-color;
      transition: color 0.2s linear;
      cursor: pointer;
      &:after {
        position: absolute;
        content: "";
        left: 50%;
        bottom: 6px;
        opacity: 0;
        transform: translateY(-50%);
        width: 5px;
        height: 5px;
        border-radius: 50%;
        background-color: darken($footer-brown, 30%);
      }
      &:hover {
        &:after {
          opacity: 1;
          bottom: 2px;
          transition: bottom 0.15s linear, opacity 0.15s linear;
        }
      }
    }
  }
  @include mobile-end {
    border-bottom: unset;
    position: relative;
    &::after {
      position: unset;
      content: unset;
      left: unset;
      transform: unset;
      width: unset;
      height: unset;
      background-color: unset;
    }
    .links {
      padding: unset;
      position: fixed;
      width: 100%;
      max-width: 250px;
      height: 100vh;
      margin: unset;
      display: block;
      background-color: $main-background;
      width: 72px;
      padding-right: 7px;
      padding-top: 6px;
      border-right: 1px solid lighten($header-color, 20%);
      a {
        text-decoration: none;
        .btns {
          transform: unset;
          padding: 4px 0;
          font-size: 14px;
          transform: translateX(-70px);
          opacity: 0;
          margin-left: auto;
          margin-bottom: 3px;
          display: block;
          &::after {
            top: 50%;
            left: 0;
            transform: translateY(-50%);
          }
          &:hover {
            &::after {
              opacity: 1;
              left: -8px;
              transition: left 0.15s linear, opacity 0.15s linear;
            }
          }
        }
      }
    }
  }
  @include desktop-large {
    position: fixed;
    height: 44px;
    width: 100%;
    background-color: $main-background;
    &::after {
      position: absolute;
      content: "";
      left: 50%;
      transform: translateX(-50%);
      width: 1680px;
      height: 1px;
      background-color: lighten($header-color, 20%);
    }
    .links {
      border: unset;
      position: relative;
      padding-right: unset;
      width: 100%;
      height: 44px;
      padding-top: 10px;
      margin: auto;
      display: flex;
      align-items: center;
      justify-content: space-between;
      a {
        .btns {
          margin-left: unset;
          transform: unset;
          transform: translateY(-50px);
          padding: 5px 12px 15px 12px;
          &:after {
            top: unset;
            bottom: 6px;
            left: 50%;
            transform: translateY(-50%);
          }
          &:hover {
            &:after {
              top: unset;
              left: 50%;
              transform: translateY(-50%);
              bottom: 2px;
              transition: bottom 0.15s linear, opacity 0.15s linear;
            }
          }
        }
      }
    }
  }
}
</style>
