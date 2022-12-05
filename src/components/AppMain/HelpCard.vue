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
        &:nth-child(2n){
            align-self: flex-end;
            padding-top: 70px;
        }
        &:not(:nth-child(2n)) img{
            height: 100px;
        }
    }
</style>