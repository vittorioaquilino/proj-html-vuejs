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
            linksFooter: [
                {
                    url: "#",
                    title: "about",
                    description: [
                        {
                            text: "Sed nec felis pellentesque, lacinia dui sed, ultricies sapien. Pellentesque orci lectus, consecteur vel, rutrum eu ipsum. Mauris accumsan eros eget libero posuere vulputate."
                        },
                    ]
                },
                {
                    url: "#",
                    title: "contact",
                    description: [
                        {
                            text: "USA, California 20, First Avenue, California",
                            number: "Tel.:+1 212 458 300 32 Fax.:+1 212 375 24 14",
                            email: "info@masterstudy.com"

                        },
                    ],
                },
            ],
        }
    },
}
</script>

<style lang="scss">
@import "./style/common.scss";


</style>
