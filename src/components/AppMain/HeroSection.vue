heroSection/<script>
import CommonButton from '../common/CommonButton.vue';

export default {
    name: "HeroSection",
    components: {
        CommonButton
    }
}
</script>

<template>
    <section class="hero">
        <a id="top" name="top"></a>
        <div class="hero__details">
            <h2 class="subtitle">Hello, Im Matin</h2>
            <h2>Artist Coaching And Mentoring Might Be for You.</h2>
            <CommonButton class="get-started-button mt-4" textButton="Get started today"/>
        </div>
        <div class="hero__shortcuts">
            <a href="#">
                <i class="fa-solid fa-ruler-combined"></i>
            </a>
            <a href="#">
                <i class="fa-solid fa-bullseye"></i>
            </a>
            <a href="#">
                <i class="fa-solid fa-book"></i>
            </a>
            <a href="#">
                <i class="fa-solid fa-cart-shopping"></i>
            </a>
        </div>

        <div class="image-details">
            <!-- Details left -->
            <img class="flowers" src="/src/assets/heroSection/artist-course-06-480x480.jpg" alt="">
            <img class="artist-shape-left-2" src="/src/assets/heroSection/artist-shape-02-600x324.png" alt="detail">
            <img class="artist-shsape-left-3" src="/src/assets/heroSection/artist-shape-03.png" alt="">
            <img class="artist-face" src="/src/assets/heroSection/artist-hero-image-03-204x300.png" alt="">
            <img class="artist-multi-color" src="/src/assets/heroSection/artist-hero-image-02-232x300.jpg" alt="">
            <img class="artist-monkey" src="/src/assets/heroSection/artist-hero-image-01.jpg" alt="">
            
            <!-- Details right -->
            <img class="artist-shape-right-1" src="/src/assets/heroSection/artist-shape-01-600x577.png" alt="detail">
            <img class="leaf" src="/src/assets/heroSection/leaf.png" alt="">
            <img class="color-shades" src="/src/assets/heroSection/artist-shape-05-300x198.png" alt="">
            <img class="color-shades-2" src="/src/assets/heroSection/artist-shape-color-paint-top-left-300x170.png" alt="">
            <img class="dotted-img" src="/src/assets/heroSection/maxcoach-shape-05.png" alt="">
            <img class="boy-picture" src="src/assets/heroSection/artist-hero-image-04-235x300.jpg" alt="">
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .hero{
        background-color: #fbf9f6;
        padding: 195px 0;
        position: relative;
        & .image-details > img{
            position: absolute;
            &.artist-shape-left-2{
                width: 680px;
                top: 0;
                left: 0;
            }
            &.flowers{
                width: 180px;
                height: 180px;
                bottom: 190px;
                left: 10px;
            }
            &.artist-shsape-left-3{
                width: 280px;
                top: 95px;
            }
            &.artist-multi-color{
                max-width: 200px;
                top: 70px;
                left: 280px;
            }
            &.artist-monkey{
                max-width: 170px;
                top: 295px;
                left: 120px;
            }
            &.artist-shape-right-1{
                width: 650px;
                height: 510px;
                top: 0;
                right: 50px;
            }
            &.artist-face{
                max-width: 11%;
                top: 260px;
                left: 380px;
            }
            &.leaf{
                max-width: 100px;
                top: 50px;
                right: 82px;
                rotate: 5deg;
            }
            &.color-shades{
                right: 0;
                bottom: 0;
            }
            &.color-shades-2{
                rotate: 90deg;
                right: 175px;
                bottom: 150px;
            }
            &.dotted-img{
                right: 200px;
                bottom: 35px;
            }
            &.boy-picture{
                bottom: 60px;
                right: 150px;
            }
        }
        & .hero__details{
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100%;
            & h2{
                width: 29.375rem;
                text-align: center;
            }
            & .get-started-button{
                padding: .625rem 1.875rem;
            }
        }
        & .hero__shortcuts{
            position: absolute;
            top: 70px;
            right: 0;
            width: 40px;
            height: 160px;
            background-color: white;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-around;
            border-radius: 8px;
            box-shadow: 0 0 50px black;
            & a{
                color: black;
            }
        }
    }
    // Link che porta all'inizio della pagina
    #top{
        position: absolute;
        top: -200px;
    }
</style>