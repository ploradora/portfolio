<template>
  <section>
    <p>Work</p>
    <div class="grid-container">
      <h1>Journal</h1>
      <article class="about-journal">
        <p class="p-journal p1-journal">
          Journal is a personal project that started off with small ideas drawn
          on paper and tiny bursts of inspiration coming in at the same time. My
          main focus was to build a project that would combine the exercises I
          have completed in the past few months whilst taking JavaScript, Vue JS
          and Firebase courses. The idea of a journal app came about after
          watching the docu series on Andy Warhol’s life based on its diaries he
          kept in his later years.
        </p>
        <p class="p-journal p2-journal">
          The goal was to create a clean and simple design including small
          touches of transitions. At its core resembling the functionality of a
          physical journal one would keep and write in, removing the
          distractions of a typical social media platform. Meaning no sharing,
          liking or having a friends list, making it more of a private
          application by being accessible only to the user holding an account on
          Journal.
        </p>
        <p class="p-journal p3-journal">
          A large portion of the concept was completed in Figma in a little over
          a week. Small details and tweaks were added on the fly. The entirety
          of the website was done in under 2 months.
        </p>
      </article>
      <a class="journal-link" href="">
        <img
          src="../assets/images/project-ss/journal-ss.png"
          alt="journal app screen shot"
        />
      </a>
      <h1>Other Projects</h1>
      <article class="other-projects">
        <p class="p-projects p1-projects">
          Here are a few selections of exercises made from the
          <a class="inline-link" href="">frontend mentor’s website</a> . Each of
          these small projects solves a problem. With tools such as images,
          icons, colors, fonts and final design looks for each media type
          already being provided
        </p>
        <p class="p-projects p2-projects">
          I was able to focus entirely on writing the code, getting the projects
          as close as possible to the final look as well as being easly readable
          for other developers.
        </p>
      </article>
      <div class="projects-grid">
        <div class="project-container">
          <a target="_blank" href="">
            <img
              src="../assets/images/project-ss/ecommerce-mobile.jpg"
              alt="shoe e-commerce project screenshot"
            />
          </a>
          <div class="buttons">
            <button>
              <a href="">Project</a>
            </button>
            <button>
              <a href="">GitHub</a>
            </button>
          </div>
        </div>
        <div class="project-container">
          <a target="_blank" href="">
            <img
              src="../assets/images/project-ss/tip-mobile.jpg"
              alt="tip calculator project screenshot"
            />
          </a>
          <div class="buttons">
            <button>
              <a href="">Project</a>
            </button>
            <button>
              <a href="">GitHub</a>
            </button>
          </div>
        </div>
        <div class="project-container">
          <a target="_blank" href="">
            <img
              src="../assets/images/project-ss/todo-mobile.jpg"
              alt="to do project screenshot"
            />
          </a>
          <div class="buttons">
            <button>
              <a href="">Project</a>
            </button>
            <button>
              <a href="">GitHub</a>
            </button>
          </div>
        </div>
        <div class="project-container">
          <a target="_blank" href="">
            <img
              src="../assets/images/project-ss/tracking-mobile.jpg"
              alt="time tracking website project screenshot"
            />
          </a>
          <div class="buttons">
            <button>
              <a href="">Project</a>
            </button>
            <button>
              <a href="">GitHub</a>
            </button>
          </div>
        </div>
        <div class="project-container">
          <a target="_blank" href="">
            <img
              src="../assets/images/project-ss/space-mobile.jpg"
              alt="space website project screenshot"
            />
          </a>
          <div class="buttons">
            <button>
              <a href="">Project</a>
            </button>
            <button>
              <a href="">GitHub</a>
            </button>
          </div>
        </div>
        <div class="project-container">
          <a target="_blank" href="">
            <img
              src="../assets/images/project-ss/furniture-mobile.jpg"
              alt="furniture website project screenshot"
            />
          </a>
          <div class="buttons">
            <button>
              <a href="">Project</a>
            </button>
            <button>
              <a href="">GitHub</a>
            </button>
          </div>
        </div>
      </div>
      <h1>Drawings</h1>
      <p class="p-drawings">
        The following is a selection of a few digital drawings made over the
        last couple of months on Procreate.
      </p>
      <div class="drawings-slide">
        <img
          src="../assets/images/grey-man-1.jpg"
          alt="digital portrait of a man"
        />
        <img
          src="../assets/images/ben-kitty.jpg"
          alt="digital portrait of benjamin franklin"
        />
        <img
          src="../assets/images/blue-lady.jpg"
          alt="digital portrait of an old woman"
        />
        <img
          src="../assets/images/cowboys.jpg"
          alt="digital portrait of a man wearing a hat"
        />
        <img
          src="../assets/images/green-cowboys.jpg"
          alt="digital portrait of a man wearing a hat"
        />
        <img
          src="../assets/images/purple-girl.jpg"
          alt="digital portrait of an young girl"
        />
        <img
          src="../assets/images/sketch-detail.jpg"
          alt="digital portrait of woman's profile"
        />
        <img
          src="../assets/images/yellow-lady.jpg"
          alt="digital portrait of a Hollywood actress"
        />
      </div>
    </div>
  </section>
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
@import "../assets/globalStyles.scss";
section {
  position: relative;
  min-height: 100vh;
  // background-color: cadetblue;
  overflow: hidden;
  font-family: $ff;
  > p {
    color: $header-color;
    font-size: 17px;
    font-weight: 500;
    text-align: end;
    padding-right: 5%;
    margin-top: 10px;
  }
  .grid-container {
    margin: auto;
    width: 90%;
    // .drawings-slide {
    //   position: absolute;
    //   left: 0;
    //   right: 0;
    //   bottom: 0;
    //   height: 80vh;
    //   overflow: auto;
    //   overflow-y: hidden;
    //   white-space: nowrap;
    // }
    h1 {
      font-size: 40px;
      margin-top: 50px;
      color: $header-color;
    }
    .about-journal {
      margin-top: 30px;
      margin-bottom: 15px;
      font-size: 15px;
      color: $body-color;
      p {
        line-height: normal;
        margin-bottom: 15px;
      }
      p:last-child {
        margin-bottom: unset;
      }
    }
    .journal-link {
      background-color: red;
      user-select: none;
      cursor: pointer;
      img {
        width: 100%;
        height: 100%;
        display: block;
        border-radius: 7px;
        border: 1px solid $header-color;
        object-fit: cover;
        object-position: center;
        transition: all 0.15s linear;
        &:hover {
          transform: scale(1.001);
          box-shadow: 0px 7px 7px 2px rgba(70, 70, 70, 0.18);
          transition: all 0.15s linear;
        }
      }
    }
    .other-projects {
      margin-top: 30px;
      font-size: 15px;
      color: $body-color;
      p {
        line-height: normal;
        margin-bottom: 15px;
        .inline-link {
          position: relative;
          text-decoration: none;
          color: darken($header-color, 10%);
          font-weight: 500;
          &::after {
            position: absolute;
            content: "";
            left: 0;
            bottom: 0;
            width: 0;
            opacity: 0;
            height: 1px;
            left: 50%;
            transform: translateX(-50%);
            background-color: $header-color;
            transition: width 0.15s ease-in-out, opacity 0.15s ease-in-out;
          }
          &:hover {
            &::after {
              opacity: 1;
              width: 100%;
              transition: width 0.15s ease-in-out, opacity 0.15s ease-in-out;
            }
          }
        }
      }
    }
    .projects-grid {
      display: grid;
      gap: 5px;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      .project-container {
        position: relative;
        margin-bottom: 20px;
        a {
          width: 100%;
          height: 170px;
          img {
            width: 100%;
            height: 170px;
            border-radius: 4px;
            object-fit: cover;
            object-position: center;
            transition: all 0.15s ease-in-out;
            &:hover {
              box-shadow: 0px 3px 3px 1px rgba(70, 70, 70, 0.18);
              // transform: scale(1.001);
              transition: all 0.15s ease-in-out;
            }
          }
        }
        .buttons {
          padding-top: 8px;
          // height: 32.4px;
          button {
            background-color: unset;
            height: 30px;
            margin-right: 5px;
            border-radius: 3px;
            border: 2px solid $green3;
            font-family: $ff;
            font-size: 15px;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.15s ease-in-out;
            &:hover {
              background-color: darken($green3, 10%);
              border-color: darken($green3, 10%);
              transition: all 0.15s ease-in-out;
            }
            a {
              text-decoration: none;
              padding: 7px 15px;
              color: $green4;
              transition: all 0.15s ease-in-out;
              &:hover {
                color: $main-background;
                transition: all 0.15s ease-in-out;
              }
            }
          }
        }
      }
    }
  }
  // img {
  //   width: 100%;
  //   height: 100%;
  //   object-fit: cover;
  //   object-position: center center;
  // }
  @include mobile-end {
    > p {
      padding-right: 10px;
    }
  }
}
</style>
