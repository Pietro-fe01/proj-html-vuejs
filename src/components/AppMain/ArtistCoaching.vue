<script>
import HelpCard from './HelpCard.vue'
export default {
    name: 'ArtistCoaching',
    components: {
        HelpCard
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
    <section class="artist-coaching pt-5">
        <div class="container">
            <div class="title pb-5">
                <h2 class="subtitle">Artist coaching</h2>
                <h2>I understand what it takes to create. <br/> I can help you with</h2>
            </div>
            <div class="cards pb-5">
                <HelpCard
                v-for="help in helpList"
                :info="help"/>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .title{
        text-align: center;
    }
    .cards{
        display: flex;
    }
</style>