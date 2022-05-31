<template>
  <section class="news-letter mt-5">
      <div class="container">
          <div class="row">
              <div class="col-7">
                  <h4>Subscribe our newsletter</h4>
                  <p>There aremany variationsof passages of Lorem Ipsum available, but the majority have suffered alteration  in some form, by injected humour, or randomised words</p>
              </div>
              <div class="col-5">
                  <p class="text-uppercase">your e-mail address</p>
                  <input type="text" placeholder="Enter your E-mail">
                  <span class="text-uppercase">subscribe</span>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name: "AppNewsLetter",
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.news-letter {
    width: 100%;
    background-color: $brand-primary-color;
    color: white;
    padding-top: 2rem;
    padding-left: 8rem;
    padding-bottom: 2rem;

    input {
        border: none;
        background-color: #eff2f5;
        width: 350px;
        padding: .7rem;
    }

    span {
       padding: .9rem;
        background-color: $brand-secondary-color;
        line-height: 50px;
        text-align: center;
        color: lightgray;
    }
}

</style>