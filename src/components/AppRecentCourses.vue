<template>
  <section>
      <!-- title -->
      <h1 class="text-center fw-bold mt-5">Recent Courses</h1>
      <!-- courses menu -->
      <ul class="courses-menu d-flex">
          <li 
          v-for="(element, index) in recentCoursesMenu"
          :key="index"
          :class="recentCoursesMenu[index].active ? 'active' : ''"
          >
              <a href="">{{ element.text }}</a>
          </li>
      </ul>
      <!-- courses card -->
      <div class="courses-card">
              <ul class="d-flex card-list">
                  <li
                  v-for="(element, index) in card"
                  :key="index"
                  class="mt-5"
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
          <!-- button -->
          <div class="button d-flex">
            <button class="first-button fw-bold text-uppercase">show all</button>
          </div>
  </section>
</template>

<script>
export default {
    name: "AppRecentCourses",
    props: {
        recentCoursesMenu: Array,
    },
    data() {
        return {
            card: [
                {
                    img:"895786_7b4b_2-544x322.jpg",
                    title: "Development>",
                    text: "The Complete iOS 10 & Swift 3 Developer Course",
                    vote: 8,
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
                    vote: 8,
                    oldprice: "$89.99",
                    newprice: "$45",
                },
                {
                    img: "949316_2a64_11-272x161.jpg",
                    title: "Development>",
                    text: "Foundations for Mastering Watercolor Painting",
                    vote: 9.5,
                    oldprice: "$19.99",
                    newprice: "$10",
                },
                {
                    img: "366802_6fcc-272x161.jpg",
                    title: "Development>",
                    text: "Get Wine-Smart",
                    vote: 8,
                    oldprice: "$49.99",
                    newprice: "$25",
                },
                {
                    img: "381588_2e6d_4-272x161.jpg",
                    title: "Development>",
                    text: "The Colored Pencil Drawing Course",
                    vote: 8,
                    oldprice: "$34.99",
                    newprice: "$18",
                },
                {
                    img: "838056_611a_3-272x161.jpg",
                    title: "Development>",
                    text: "Paint Realistic Wtercolor and Botanicals - STUDIO BASICS",
                    vote: 8,
                    oldprice: "$69.99",
                    newprice: "$35",
                },
                {
                    img: "1414956_d944_15-272x161.jpg",
                    title: "Development>",
                    text: "Mastering Brushstrokes - Part 1",
                    vote: 9.5,
                    oldprice: "$19.99",
                    newprice: "$10",
                },
                {
                    img: "1109398_4c13-272x161.jpg",
                    title: "Development>",
                    text: "Paint Realistic Wtercolor and Botanicals - MAGNOLIAS",
                    vote: 9.5,
                    oldprice: "$69.99",
                    newprice: "$35",
                }
            ],
        }
    },
    methods: {
        convertVote(vote) {
            const convertedVote = vote / 2;
            const roundedVote = Math.ceil(convertedVote);
            return roundedVote;
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.courses-menu {
    justify-content: center;
    margin-top: 2rem;

    li {
        margin: 0 1.5rem;
        padding: .5rem;
    }

    a {
        color: gray;
    }

    .active {
        background-color: #dde6eb;
        border-radius: 30px;
    }
}

.card-list {
    flex-wrap: wrap;
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

      .price-vote i {
          font-size: .8rem;
          color: $brand-star-color;
      }
        
}

.button {
    justify-content: center;
}

.first-button {
    padding: .7rem;
    border-radius: 30px;
    color: white;
    background-color: $brand-primary-color;
    border: none;
    margin: 3rem .5rem;
}
    
.first-button:hover {
    border: 1px solid $brand-primary-color;
    color: $brand-primary-color;
    background-color: white;
}

h1 {
    font-size: 3rem;
}

</style>