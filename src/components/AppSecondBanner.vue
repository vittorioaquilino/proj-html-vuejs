<template>
    <section class="second-banner">
        <div class="row">
            <div class="col-6 banner-text">
                <h1 class="fw-bold">Limitless learning, more possibilities</h1>
                <p>Online courses open the opportunity for learning to almost anyone, regardlessof their scheduling commitments.</p>
                <button class="first-button text-uppercase fw-bold">read more</button>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "AppSecondBanner",
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.second-banner {
    background-image: url("../assets/images/bg.png");
    height: 500px;
    background-position: center;
    margin-top: 4rem;

    .banner-text {
        padding-top: 8rem;
        padding-left: 15rem;

        h1 {
            font-size: 3rem;
        }
    }

    .first-button {
        padding: .7rem;
        border-radius: 30px;
        color: white;
        background-color: $brand-primary-color;
        border: none;
        margin: 0 .5rem;

    }
    
    .first-button:hover {
        border: 1px solid $brand-primary-color;
        color: $brand-primary-color;
        background-color: white;
    }
}
</style>