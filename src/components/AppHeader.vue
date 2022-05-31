<template>
  <header class="ms_header">
      <div class="container">
          <!-- header top -->
          <div class="ms_header-top">
              <!-- language -->
              <div class="ms_header-language">
                  <span class="m-2">English</span>
                  <i class="fas fa-angle-down"></i>
              </div>
              <!-- menu -->
              <div class="ms_header-menu">
                  <ul class="menu-list d-flex mt-2">
                      <li
                      v-for="(element, index) in headerMenu"
                      :key="index"
                      >
                        <a href="">{{ element.text }}</a>
                      </li>
                      <!-- social -->
                      <li><i class="fab fa-facebook"></i></li>
                      <li><i class="fab fa-twitter"></i></li>
                      <li><i class="fab fa-instagram"></i></li>
                      <li><i class="fab fa-linkedin"></i></li>
                      <li><i class="fab fa-google-plus"></i></li>
                      <li><i class="fab fa-youtube"></i></li>
                  </ul>
              </div>
          </div>
          <!-- /header top -->
      </div>
      <hr>
      <div class="container">
          <!-- header bottom -->
          <div class="ms_header-bottom">
              <!-- logo -->
              <div class="ms_header-logo">
                <img src="../assets/images/footer-logo2x-50x56.png" alt="">
                <span class="fw-bold">MASTER</span> <span>STUDY</span>
              </div>
              <!-- search -->
              <div class="ms_header-search">
                  <!-- category -->
                  <i class="fas fa-bars"></i>
                  <span class="text-uppercase fw-bold">Category</span>
                  <!-- input -->
                  <div class="ms_input">
                    <input type="text" placeholder="Search courses">
                    <i class="fas fa-search"></i>
                  </div>
                  <!-- login -->
                  <div class="ms_login">
                      <i class="fas fa-bullhorn"></i>
                      <span>Became and Instructor</span>
                      <i class="fas fa-briefcase"></i>
                      <span>For Entreprise</span>
                      <div class="user-login">
                          <i class="fas fa-user"></i>
                          <span>Login</span>
                          <button class="text-uppercase fw-bold first-button">sign up</button>
                          <i class="far fa-bookmark"></i>
                      </div>
                  </div>
              </div>
          </div>
          <!-- /header bottom -->
      </div>
  </header>
</template>

<script>
export default {
    name: "AppHeader",
    props: {
        headerMenu: Array,
    },
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.ms_header {
    width: 100%;
    height: 200px;

    &-top {
        height: 70px;
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
        display: flex;
        align-items: center;
        width: 100%;
        margin: auto;

        img {
            background-color: $brand-primary-color;
            margin-right: .5rem;
        }

        .ms_header-logo {

            span {
                font-size: 1.5rem;
            }
        }

        .ms_header-search {
            color: gray;
            display: flex;
            align-items: center;
            margin-left: 2rem;

            span {
                font-size: .7rem;
            }

            input {
                border: none;
                background-color: #eff2f5;
                width: 350px;
                padding: .7rem;
                margin-left: 1rem;
            }

            .ms_input i {
                width: 60px;
                height: 48px;
                background-color: $brand-secondary-color;
                line-height: 50px;
                text-align: center;
                color: lightgray;
            }
        }

        .ms_login {
            display: flex;
            align-items: center;

            i {
                margin: 0 .4rem;
                color: #447991;
            }

            span {
                font-size: .9rem;
            }

            .user-login {
                margin-left: 2rem;

                .first-button {
                    padding: .7rem;
                    border-radius: 30px;
                    color: white;
                    background-color: $brand-primary-color;
                    border: none;
                    margin: 0 .5rem;
                }
            }
        }
    }

    hr {
        width: 100%;
        margin: 0;
    }
}
</style>