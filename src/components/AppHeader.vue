<template>
  <header class="ms_header">
      <div class="container">
          <div class="ms_header-top">
              <div class="ms_header-language">
                  <span class="m-2">English</span>
                  <i class="fas fa-angle-down"></i>
              </div>
              <div class="ms_header-menu">
                  <ul class="menu-list d-flex mt-2">
                      <li
                      v-for="(element, index) in links"
                      :key="index"
                      >
                        <a href="">{{ element.text }}</a>
                      </li>
                      <li><i class="fab fa-facebook"></i></li>
                      <li><i class="fab fa-twitter"></i></li>
                      <li><i class="fab fa-instagram"></i></li>
                      <li><i class="fab fa-linkedin"></i></li>
                      <li><i class="fab fa-google-plus"></i></li>
                      <li><i class="fab fa-youtube"></i></li>
                  </ul>
              </div>
          </div>
      </div>
      <hr>
      <div class="container">
          <div class="ms_header-bottom"></div>
      </div>
  </header>
</template>

<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    url: "#",
                    text: "Home"
                },
                {
                    url: "#",
                    text: "Pages"
                },
                {
                    url: "#",
                    text: "Course Formats"
                },
                {
                    url: "#",
                    text: "Courses"
                },
                {
                    url: "#",
                    text: "Demos"
                },
            ],
        }
    },
    components: {

    }
}
</script>

<style lang="scss" scoped>

.ms_header {
    width: 100%;
    height: 200px;

    &-top {
        height: 70px;
        border: 1px solid red;
        display: flex;
        justify-content: space-between;
        align-items: center;
        font-size: .9rem;
        color: gray;

        li {
            margin: 0 .5rem;
        }
    }

    &-bottom {
        height: 130px;
        border: 1px solid green;
    }

    hr {
        width: 100%;
        margin: 0;
    }
}
</style>