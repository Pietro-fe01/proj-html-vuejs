<script>
export default {
    name: 'HelpCard',
    props: {
        info: Object
    }
}
</script>

<template>
    <div class="ms-card">
        <img :src="`/src/assets/artistCoaching/${info.helpImage}`" alt="">
        <h4 class="mt-3">{{info.helpType}}</h4>
        <p>{{info.description}}</p>
    </div>
</template>

<style lang="scss" scoped>
    .ms-card{
        width: calc(100% / 4 - 20px);
        & img{
            max-width: 40%;
        }
        & h4{
            font-weight: bolder;
        }
        &:not(:nth-child(2n)) img{
            height: 100px;
        }
    }

    /*--------------------
        RESPONSIVE
    --------------------*/
    @media screen and (min-width: 576px) {
        .ms-card{
            width: 100%;
            padding-bottom: 50px;
        }
    }

    @media screen and (min-width: 768px) {
        .ms-card{
            width: calc(100% / 2 - 20px);
            &:nth-child(2n){
                align-self: flex-end;
                padding-top: 70px;
            }
        }
    }

    @media screen and (min-width: 1200px) {
        .ms-card{
            width: calc(100% / 4 - 20px);
        }
    }
</style>