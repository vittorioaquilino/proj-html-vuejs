<template>
    <section>
      <!-- pre footer -->
      <AppPreFooter />
      <!-- /pre footer -->

      <div class="ms_footer">
        <div class="footer-top">
           <div class="container">
            <div class="row">
              <div class="col-3">
                <h4>{{footerMenu.about.title }}</h4>
                <p>{{ footerMenu.about.text }}</p>
              </div>
              <div class="col-3">
                <h4>{{footerMenu.contact.title }}</h4>
                <p>{{ footerMenu.contact.address }}</p>
                <p>{{ footerMenu.contact.number }}</p>
                <p>{{ footerMenu.contact.fax}}</p>
                <p class="mail">{{ footerMenu.contact.mail }}</p>
              </div>
              <div class="col-3">
                <h4>{{footerMenu.social.title }}</h4>
                <i class="fab fa-facebook icon1"></i>
                <i class="fab fa-instagram icon2"></i>
                <i class="fab fa-linkedin icon3"></i>
                <i class="fab fa-pinterest icon4"></i>
                <i class="fab fa-twitter icon5"></i>
                <i class="fas fa-basketball-ball icon6"></i>
                <i class="fab fa-google-plus icon7"></i>
                <i class="fab fa-skype icon8"></i>
              </div>
              <div class="col-3">
                <img src="../assets/images/Top-udemy-courses-90-percent-off.jpg" alt="">
              </div>
            </div>
          </div>
        </div>
        <hr>
        <div class="footer-bottom d-flex">
          <div class="container">
            <img  class="logo" src="../assets/images/footer-logo2x-50x56.png" alt="">
            <span>Copyright &copy; 2020. <a href="">MasterStudy.</a> Theme by <a href="">StylemixThemes.</a></span>
          </div>
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
      footerMenu: Object,
    }
}
</script>

<style lang="scss" scoped>
.ms_footer {
  background-color: #273043;
  padding-top: 3rem;
  padding-bottom: 3rem;
  color: white;
}

h4 {
  text-transform: uppercase;
  margin-bottom: 1.5rem;
  font-size: 1.2rem;
}

img {
  width: 100%;
}

i {
  width: 50px;
  margin-bottom: 2rem;
  margin-right: 1rem;
  font-size: 1.5rem;
  border-radius: 30px;
  padding: .7rem;
  text-align: center;
}

.mail {
  color: gray;
}

p {
  font-size: .8rem;
}

.icon1 {
  background-color: #3c5998;
}

.icon2 {
  background-color: #c22aa3;
}

.icon3 {
  background-color: #0177b5;
}

.icon4 {
  background-color: #bd091c;
}

.icon5 {
  background-color: #1da1f1;
}

.icon6 {
  background-color: #e94c89;
}

.icon7 {
  background-color: #da4437;
}

.icon8 {
  background-color: #01aef0;
}
.footer-bottom {
  height: 50px;
  align-items: center;
  justify-content: center;

  span,
  a {
    font-size: .8rem;
    color: white;
  }
}

.logo {
  width: 30px;
  margin-right: 1rem;

}

</style>