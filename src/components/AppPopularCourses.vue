<template>
  <section class="popular-courses">
      <!-- title -->
      <h1 class="fw-bold text-center">Popular courses</h1>
      <p class="text-center mb-4">Discover our most popular courses for self learning</p>
      <div class="courses-card">
              <ul class="d-flex card-list">
                  <li
                  v-for="(element, index) in card"
                  :key="index"
                  >
                  <!-- images -->
                    <img :src="require(`../assets/images/${element.img}`)" alt="">
                    <!-- description -->
                    <div class="description">
                        <p class="card-title">{{ element.title }}</p>
                        <p class="card-text">{{ element.text }}</p>
                    </div>
                    <!-- price -->
                    <div class="price">
                        <div class="price-vote">
                            <img class="star" src="../assets/images/starfull.svg" alt="">
                        </div>
                        <div class="price-number">
                            <p class="old">{{ element.oldprice }}</p>
                            <p class="text-end">{{ element.newprice }}</p>
                        </div>
                    </div>
                  </li>
              </ul>
          </div>
          <div class="before-next d-flex">
            <div class="left text-center">
                <i class="fas fa-angle-left"></i>
            </div>
            <div class="right text-center">
                <i class="fas fa-angle-right"></i>
            </div>
          </div>
  </section>
</template>

<script>
export default {
    name: "AppPopularCourses",
    data() {
        return {
            card: [
                {
                    img:"895786_7b4b_2-544x322.jpg",
                    title: "Development>",
                    text: "The Complete iOS 10 & Swift 3 Developer Course",
                    vote: 9,
                    oldprice: "$199.99",
                    newprice: "$100",
                },
                {
                    img: "1561458_7f3b-272x161.jpg",
                    title: "Development>",
                    text: "CSS - The Complete Guide 2020 (incl. Flexbox, Grid & Sass)",
                    vote: 9,
                    oldprice: "$199.99",
                    newprice: "$100",
                },
                {
                    img: "246154_d8b0_3-272x161.jpg",
                    title: "Development>",
                    text: "Web Design for Beginners: Real World Codin in HTML & CSS",
                    vote: 9.5,
                    oldprice: "$129.99",
                    newprice: "$65",
                },
                {
                    img: "1208228_d61c_4-272x161.jpg",
                    title: "Development>",
                    text: "Digitally Painting Light and Color : Amateur to Master",
                    vote: 9.5,
                    oldprice: "$139.99",
                    newprice: "$70",
                },
                {
                    img: "186792_41e4_4-272x161.jpg",
                    title: "Development>",
                    text: "Became an Arabic CalligraphyArtist from Scratch",
                    vote: 9.5,
                    newprice: "$199.99",
                },
                {
                    img: "1776542_30b1-272x161.jpg",
                    title: "Development>",
                    text: "Google Searching Ninja!",
                    vote: 9.5,
                    oldprice: "$89.99",
                    newprice: "$45",
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.popular-courses {
    padding-top: 5rem;
    padding-bottom: 3rem;
    background-color: #f0f4f9;

    h1 {
        font-size: 3rem;
    }
}

.courses-card li {
    width: calc(100% / 6 - 10px);
    border: 1px solid lightgray;
    margin: 5px;

    img {
        width: 100%;
        margin-bottom: .5rem;
    }

    .description {
        padding: .7rem;

        .card-title {
        font-size: .8rem;
        color: lightgray;
        }

        .card-text {
            font-size: .8rem;
            padding-bottom: .5rem;
            border-bottom: 1px solid lightgray;
            }
        }

        .price {
            padding: .7rem;
            display: flex;
            justify-content: space-between;
            
            .star {
                width: 15px;
            }

            .price-number {
                font-size: .8rem;

                .old {
                    text-decoration: line-through;
                    color: lightgray;
                    margin: 0;
                }
            }
      }
        
}

.before-next {
    justify-content: center;

    .left,
    .right {
        width: 40px;
        height: 40px;
        border: 1px solid lightgray;
        line-height: 40px;
        color: lightgray;
    }

    .left:hover,
    .right:hover {
        background-color: $brand-secondary-color;
        color: white;
    }
}

</style>