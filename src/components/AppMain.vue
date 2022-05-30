<template>
    <section class="ms_main">
      <!-- pre banner -->
      <AppPreBanner />
      <!-- /pre banner -->

      <!-- banner -->
      <AppBanner />
      <!-- /banner -->
    </section>
</template>

<script>
import AppPreBanner from "./AppPreBanner.vue";
import AppBanner from "./AppBanner.vue";

export default {
    name: "AppMain",
    components: {
        AppPreBanner,
        AppBanner,
    }
}
</script>

<style lang="scss" scoped> 

</style>