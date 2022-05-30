<template>
    <section class="ms_main">
      <!-- pre banner -->
      <AppPreBanner />
      <!-- /pre banner -->

      <!-- banner -->
      <AppBanner />
      <!-- /banner -->

      <!-- popular courses -->
      <AppPopularCourses />
      <!-- /popular courses -->
    </section>
</template>

<script>
import AppPreBanner from "./AppPreBanner.vue";
import AppBanner from "./AppBanner.vue";
import AppPopularCourses from "./AppPopularCourses.vue";

export default {
    name: "AppMain",
    components: {
        AppPreBanner,
        AppBanner,
        AppPopularCourses,
    }
}
</script>

<style lang="scss" scoped> 

</style>