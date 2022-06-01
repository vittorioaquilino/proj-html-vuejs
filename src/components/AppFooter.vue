<template>
    <section>
      <!-- pre footer -->
      <AppPreFooter />
      <!-- /pre footer -->

      <div class="ms_footer">
        <div class="container">
        <ul class="footer-list d-flex">
          <li 
          v-for="(element, index) in footerMenu"
          :key="index"
          >
            <a class="fw-bold text-uppercase" href="">{{ element.title }}</a>
            <p>{{ element.description[0].text }}</p>
            <p>{{ element.description[0].number }}</p>
            <p>{{ element.description[0].email }}</p>
          </li>
        </ul>

        </div>
      </div>

    </section>
</template>

<script>
import AppPreFooter from "./AppPreFooter.vue";

export default {
    name: "AppFooter",
    components: {
      AppPreFooter,
    },
    props: {
      footerMenu: Array,
    }
}
</script>

<style lang="scss" scoped>
.footer-list {
 justify-content: space-around;
}

</style>