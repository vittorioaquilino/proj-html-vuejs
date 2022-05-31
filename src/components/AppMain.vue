<template>
    <section class="ms_main">
        <!-- pre banner -->
        <AppPreBanner />
        <!-- /pre banner -->

        <!-- banner -->
        <AppFirstBanner />
        <!-- /banner -->

        <!-- popular dev courses -->
        <AppPopularDevCourses />
        <!-- /popular dev courses -->

        <!-- second banner -->
        <AppSecondBanner />
        <!-- /second banner -->

        <!-- recent courses -->
        <AppRecentCourses :recentCoursesMenu="linksCourses"/>
        <!-- /recent courses -->

        <!-- newsletter -->
        <AppNewsLetter />
        <!-- /newsletter -->

        <!-- popular courses -->
        <AppPopularCourses />
        <!-- /popular courses -->
    </section>
</template>

<script>
import AppPreBanner from "./AppPreBanner.vue";
import AppFirstBanner from "./AppFirstBanner.vue";
import AppPopularDevCourses from "./AppPopularDevCourses.vue";
import AppSecondBanner from "./AppSecondBanner.vue";
import AppRecentCourses from "./AppRecentCourses.vue";
import AppNewsLetter from "./AppNewsLetter.vue";
import AppPopularCourses from "./AppPopularCourses.vue";

export default {
    name: "AppMain",
    components: {
        AppPreBanner,
        AppFirstBanner,
        AppPopularDevCourses,
        AppSecondBanner,
        AppRecentCourses,
        AppNewsLetter,
        AppPopularCourses,
    },
    data() {
        return {
            linksCourses: [
                {
                    url: "#",
                    text: "All Categories",
                    active: true,
                },
                {
                    url: "#",
                    text: "Business"
                },
                {
                    url: "#",
                    text: "Design"
                },
                {
                    url: "#",
                    text: "Development"
                },
                {
                    url: "#",
                    text: "IT & Software"
                },
                {
                    url: "#",
                    text: "Lifestyle"
                },
                {
                    url: "#",
                    text: "Marketing"
                },
                {
                    url: "#",
                    text: "Office Productivity"
                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped> 

</style>