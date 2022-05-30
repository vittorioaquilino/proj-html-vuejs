<template>
  <section class="ms_container">
      <ul class="icon-list d-flex">
            <li
            v-for="(element, index) in icons"
            :key="index"
            >
                <i :class="element.icon"></i>
                <span>{{ element.text }}</span>
            </li>
          
      </ul>
  </section>
</template>

<script>
export default {
    name: "AppPreBanner",
    data() {
        return {
            icons: [
                {
                    icon: "far fa-chart-bar",
                    text: "Business"
                },
                {
                    icon: "fas fa-palette",
                    text: "Design"
                },
                {
                    icon: "fas fa-cog",
                    text: "Development"
                },
                {
                    icon: "far fa-smile",
                    text: "Lifestyle"
                },
                {
                    icon: "fas fa-wallet",
                    text: "Office Productivity"
                },
            ]
        }
    }
    
}
</script>

<style lang="scss" scoped>

.ms_container {
    width: 100%;
    background-color: #273043;
}

.icon-list {
    width: 70%;
    height: 100px;
    align-items: center;
    justify-content: center;
    color: white;
    margin: auto;

    li {
        width: calc(100% / 5);
    }

    i {
        margin: 0 .4rem;
    }
}
</style>