<template>
  <section class="popular-courses">
      <div class="container">
          <!-- title -->
          <h4 class="mb-3">Popular Development Courses</h4>
          <!-- courses card -->
          <div class="courses-card">
              <ul class="d-flex">
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
                            <span
                            v-for="( index) in convertVote(element.vote)"
                            :key="index"
                            class="star">
                                <i class="fa-solid fa-star"></i>
                            </span>
                            <span
                            v-for="( index) in 5 - convertVote(element.vote)"
                            :key="index + 10"
                            class="star">
                                <i class="fa-regular fa-star"></i>
                            </span>
                        </div>
                        <div class="price-number">
                            <p class="old">{{ element.oldprice }}</p>
                            <p class="text-end">{{ element.newprice }}</p>
                        </div>
                    </div>
                  </li>
              </ul>
          </div>
      </div>
  </section>
</template>

<script>
export default {
    name: "AppPopularDevCourses",
    data() {
        return {
            card: [
                {
                    img:"895786_7b4b_2-272x161.jpg",
                    title: "Development>",
                    text: "The Complete iOS 10 & Swift 3 Developer Course",
                    vote: 8,
                    oldprice: "$199.99",
                    newprice: "$100",
                },
                {
                    img: "246154_d8b0_3-272x161.jpg",
                    title: "Development>",
                    text: "Web Design for Beginners: Real World Codin in HTML & CSS",
                    vote: 8,
                    oldprice: "$129.99",
                    newprice: "$65",
                },
                {
                    img: "752950_b773-272x161.jpg",
                    title: "Development>",
                    text: "GitHub Ultimate: Master Git and GitHub - Beginner to Expert",
                    vote: 8,
                    oldprice: "$99.99",
                    newprice: "$50",
                },
                {
                    img: "1253188_58f7_2-272x161.jpg",
                    title: "Development>",
                    text: "The Complete iOS 11 & Swift Developer Course - Build 20 Apps",
                    vote: 8,
                    oldprice: "$199.99",
                    newprice: "$100",
                }, 
                {
                    img: "919872_ed54_6-272x161.jpg",
                    title: "Development>",
                    text: "Android Java Masterclass - Became an App Developer",
                    vote: 8,
                    oldprice: "$99.99",
                    newprice: "$50",
                },
                {
                    img: "951684_9c1a_2-272x161.jpg",
                    title: "Development>",
                    text: "Xamarin Forms: Build Native Cross-platform Apps with C#",
                    vote: 8,
                    oldprice: "$189.99",
                    newprice: "$95",
                },
            ],
        }
    },
    methods: {
        convertVote(vote) {
            const convertedVote = vote / 2;
            const roundedVote = Math.ceil(convertedVote);
            return roundedVote;
        },
    }
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.popular-courses {
    margin-top: 4rem;

    .courses-card li {
        width: calc(100% / 6 - 10px);
        border: 1px solid lightgray;
        margin: 5px;

        img {
            width: 200px;
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
    
    .price-vote i {
        font-size: .8rem;
        color: $brand-star-color;
    }
}

</style>