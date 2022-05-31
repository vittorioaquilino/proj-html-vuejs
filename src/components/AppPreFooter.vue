<template>
  <section class="pre-footer">
      <div class="pre-footer-content">
          <h2 class="mb-4">Investing for Your Future</h2>
          <p>It is no exaggeration to say this MasterStudy experience was
            transformative-both professionally and personally. This workshop
            will long remain a high point of my life. Thanks again..... I am feeling
            energized and eager to start teaching my class next week. I can't wait
            to use all of my new teaching tools. I will absolutely recommend this
            workshop to other educators!
          </p>
          <h5>Linda Green</h5>
          <p>Product Manager, Apple Inc</p>
      </div>
  </section>
</template>

<script>
export default {
    name: "AppPreFooter",
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.pre-footer {
    background-color: $brand-background-color;
    background-image: url("../assets/images/testimonial-1-1917x640-1-1914x639.jpg");
    background-position: center;
    background-repeat: no-repeat;
    padding-top: 5rem;
    padding-left: 13rem;
    padding-bottom: 5rem;

    &-content {
        width: 700px;
        height: 500px;
        background-color: white;
        padding: 4rem;
    }

    p {
        color: gray;
    }

    h5 {
        margin-bottom: 0;
        margin-top: 2.5rem;
    }
}

</style>