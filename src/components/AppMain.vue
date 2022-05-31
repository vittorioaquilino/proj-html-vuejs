<template>
    <section class="ms_main">
      <!-- pre banner -->
      <AppPreBanner />
      <!-- /pre banner -->

      <!-- banner -->
      <AppFirstBanner />
      <!-- /banner -->

      <!-- popular courses -->
      <AppPopularCourses />
      <!-- /popular courses -->

      <!-- second banner -->
      <AppSecondBanner />
      <!-- /second banner -->

    </section>
</template>

<script>
import AppPreBanner from "./AppPreBanner.vue";
import AppFirstBanner from "./AppFirstBanner.vue";
import AppPopularCourses from "./AppPopularCourses.vue";
import AppSecondBanner from "./AppSecondBanner.vue";

export default {
    name: "AppMain",
    components: {
        AppPreBanner,
        AppFirstBanner,
        AppPopularCourses,
        AppSecondBanner,
    }
}
</script>

<style lang="scss" scoped> 

</style>