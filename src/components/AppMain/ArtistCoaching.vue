<script>
import HelpCard from './HelpCard.vue'
import CommonButton from '../common/CommonButton.vue';

export default {
    name: 'ArtistCoaching',
    components: {
        HelpCard,
        CommonButton
    },
    data(){
        return {
            helpList: [
                {
                    helpImage: 'artist-box-image-01.png',
                    helpType: 'Online Coures',
                    description: 'Online art coaching now offers you a very powerfull way to redesign your artist mind.'
                },
                {
                    helpImage: 'artist-box-image-02.png',
                    helpType: 'One to One',
                    description: 'Getting the necessary clarity about the current state to help you improve your ability.'
                },
                {
                    helpImage: 'artist-box-image-03.png',
                    helpType: 'Anywhere',
                    description: 'Access to valuable and portable program which allow you to setup and live anywhere you want.'
                },
                {
                    helpImage: 'artist-box-image-04.png',
                    helpType: 'On Time',
                    description: 'Punctuality is our top priority because it\'s an essential criteria to assess a program quality.'
                }
            ]
        }
    }
}
</script>

<template>
    <section class="artist-coaching py-5">
        <div class="container">
            <!-- Titolo -->
            <div class="title pb-5">
                <h2 class="subtitle">Artist coaching</h2>
                <h2>I understand what it takes to create. <br/> I can help you with</h2>
            </div>

            <!-- Qui verranno stampate le card in modo dinamico -->
            <div class="cards pb-5">
                <HelpCard
                v-for="help in helpList"
                :info="help"/>
            </div>

            <!-- Qui andrà la frase motivazionale -->
            <div class="motivation py-5">
                <div class="motivation__left">
                    <img src="/src/assets/artistCoaching/artist-quote-icon.png" alt="">
                    <h2>I coach and mentor visual artist, like you, to Create Like You Mean It</h2>
                    <h6 class="subtitle pt-4">Martin Garrix</h6>
                </div>
                <div class="motivation__right">
                    <p>As a coach mentor, my ultimate goal is to motivate visual artists toward insipred action. I help you you get back on track to being the productive, creative, meaningful and authentic artist you truly want to be. I support artists in crafting and living a creative life as well as feeling good about themselves and their art.</p>
                    <p>As an artist and an educator for nearly 30 years, I understand what it takes to create.</p>
                    <CommonButton class="get-started-button" textButton="Get started today"/>
                </div>
            </div>
            
            <div class="image-details pb-5">
                <img class="detail-1" src="src\assets\artist-shape-01-600x577.png" alt="">
                <img class="line" src="/src/assets/artistCoaching/maxcoach-shape-14.png" alt="">
                <img class="waves" src="/src/assets/artistCoaching/maxcoach-shape-13-150x150.png" alt="">
                <img class="big-wave" src="/src/assets/artistCoaching/artist-shape-01-300x288.png" alt="">
                <img class="big-wave-2" src="/src/assets/artistCoaching/artist-shape-01-300x288.png" alt="">
                <img class="big-wave-3" src="/src/assets/artistCoaching/artist-shape-01-300x288.png" alt="">
            </div>

            <div class="youtube-video text-center pt-4 pb-4">
                <img class="cover" src="/src/assets/artistCoaching/artist-video-poster.jpg" alt="">

                <div class="image-details">
                    <img class="video-detail" src="/src/assets/maxcoach-shape-05.png" alt="">
                    <img class="video-detail-2" src="/src/assets/maxcoach-shape-05.png" alt="">
                    <div class="ms-circle"></div>
                    <a href="#" class="youtube-icon" >
                        <img src="/src/assets/artistCoaching/icon-youtube-play.png" alt="">
                    </a>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .artist-coaching{
        position: relative;
        overflow: hidden;
        .container{
            padding-right: 100px;
            padding-left: 100px;
            .title{
                text-align: center;
            }
            .cards{
                display: flex;
                justify-content: space-between;
            }
            & .motivation{
                display: flex;
                align-items: baseline;
                &__left{
                    text-align: center;
                    width: 30%;
                    position: relative;
                    & img{
                        position: absolute;
                        top: -25px;
                        left: 50%;
                        transform: translate(-50%, -50%);
                    }
                }
                &__right{
                    width: 70%;
                    & p, button{
                        margin-left: 150px;
                    }
                    .get-started-button{
                        padding: 10px 30px;
                        background-color: rgba(239, 111, 49, 0.2);
                        color: #ef6f31;
                        font-weight: bolder;
                    }
                }
            }
            & .image-details > img{
                position: absolute;
            }
            & .detail-1{
                width: 500px;
                transform: rotate(220deg);
                top: 75px;
                left: -135px;
            }
            & .line{
                width: 100%;
                top: 80px;
                left: 0px;
                z-index: -1;
            }
            & .waves{
                top: 190px;
                right: -35px;
            }
            & .big-wave{
                width: 30%;
                bottom: -230px;
                left: -50px;
                transform: rotate(40deg);
                &-2{
                    width: 30%;
                    bottom: -230px;
                    left: 396px;
                    transform: rotate(40deg);
                }
                &-3{
                    // width: 45%;
                    // bottom: -280px;
                    // left: 840px;
                    // rotate: 40deg;
                    // transform: scaleX(-1);
                    right: -18px;
                    bottom: -125px;
                    width: 700px;
                    height: 300px;
                    rotate: 180deg;
                }
            }
            & .youtube-video{
                position: relative;
                & .cover{
                    width: 800px;
                    max-height: 400px;
                }
                & .video-detail{
                    top: -7px;
                    left: 130px;
                    z-index: -1;
                }
                & .video-detail-2{
                    bottom: 25px;
                    right: 80px;
                    z-index: -1;
                }
                & .ms-circle{
                    background-color: transparent;
                    border: 9px solid #ecc5ab;
                    border-radius: 50%;
                    width: 65px;
                    height: 65px;
                    position: absolute;
                    top: 122px;
                    right: 108px;
                }
                & .youtube-icon{
                    top: 50%;
                    left: 50%;
                    transform: translate(-50%, -50%);
                    position: absolute;
                    & img{
                        max-width: 80px;
                    }
                }
            }
        }
    }
</style>