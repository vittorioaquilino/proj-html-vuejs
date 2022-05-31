<template>
  <section class="start-plan">
      <div class="container">
          <div class="row">
              <!-- col left -->
              <div class="col-6 content-plan">
                  <!-- image -->
                  <div class="plan-image">
                      <img src="../assets/images/image_box_1-221x231.png" alt="">
                  </div>
                  <!-- text -->
                  <div class="plan-text">
                    <h2>Become an Istructor</h2>
                    <p>Teach what you love. Masterstudy gives you the tools to create a course.</p>
                    <button class="first-button fw-bold text-uppercase">start teaching</button>
                  </div>
              </div>
              <!-- col right -->
              <div class="col-6 content-plan">
                  <!-- image -->
                  <div class="plan-image">
                      <img src="../assets/images/image_box_2-234x231.png" alt="">
                  </div>
                  <!-- text -->
                  <div class="plan-text">
                    <h2>Access for Business</h2>
                    <p>Get unlimited access to 2,500 of top courses for your team.</p>
                    <button class="first-button fw-bold text-uppercase">doing business</button>
                  </div>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name: "AppStartPlan",
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.start-plan {
    padding: 3rem;

    .content-plan {
        border: 1px solid lightgray;
        width: calc(100% / 2 - 20px);
        margin: 10px;
        padding: 2rem;
        display: flex;

        p {
            color: gray;
        }

        .plan-text {
            padding: 2rem;
        }

        .first-button {
            padding: .7rem;
            border-radius: 30px;
            color: white;
            background-color: $brand-primary-color;
            border: none;
            margin-top: .5rem;
        }
            
        .first-button:hover {
            border: 1px solid $brand-primary-color;
            color: $brand-primary-color;
            background-color: white;
        }
    }
}

</style>