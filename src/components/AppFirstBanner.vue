<template>
  <section class="ms_banner">
          <div class="row">
              <div class="col-6">
                  <h1 class="fw-bold">Udemy Affiliate Sales</h1>
                  <p>Monetize your audience and attract new customers with Udemy!</p>
              </div>
              <div class="col-6">
                  <img src="../assets/images/slide-1.jpg" alt="">
              </div>
          </div>
  </section>
</template>

<script>
export default {
    name: "AppFirstBanner",
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.ms_banner {
    margin-top: 2rem;
    background-color: $brand-primary-color;
    color: white;
    
    h1 {
        font-size: 3rem; 
        padding-top: 4rem;
        padding-left: 8rem;
    }

    p {
        font-size: 1.5rem;
        padding-left: 8rem;
    }
    img {
        width: 100%;
    }
}

</style>