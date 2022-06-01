<template>
    <div id="app">
      <!-- header -->
      <AppHeader :headerMenu="linksHeader"/>
      <!-- /header -->

      <!-- main -->
      <AppMain />
      <!-- /main -->

      <!-- footer -->
      <AppFooter :footerMenu="linksFooter"/>
      <!-- /footer -->
    </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  },
  data() {
        return {
            linksHeader: [
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
            linksFooter: {
                about: {
                    title: "about",
                    text: "Sed nec felis pellentesque, lacinia dui sed, ultricies sapien. Pellentesque orci lectus, consecteur vel, rutrum eu ipsum. Mauris accumsan eros eget libero pousere vulputate."
                },
                contact: {
                    title: "contact",
                    address: "USA, California 20, First Avenue, California",
                    number: "Tel.: +1 212 458 300 32",
                    fax: "Fax.: +1 212 375 24 14",
                    mail: "info@masterstudy.com"
                },
                social: {
                    title: "social network",
                    // icon: [
                    //     "fab fa-facebook",
                    //     "fab fa-instagram",
                    //     "fab fa-linkedin",
                    //     "fab fa-pinterest",
                    //     "fab fa-twitter",
                    //     "fas fa-basketball-ball",
                    //     "fab fa-google-plus",
                    //     "fab fa-skype",
                    // ]
                }
            }
                
        }
    },
}
</script>

<style lang="scss">
@import "./style/common.scss";


</style>
