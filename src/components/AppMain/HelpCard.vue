<script>
export default {
    name: 'HelpCard',
    props: {
        info: Object
    }
}
</script>

<template>
    <div class="card">
        <img :src="`/src/assets/artistCoaching/${info.helpImage}`" alt="">
        <h5 class="mt-3">{{info.helpType}}</h5>
        <p>{{info.description}}</p>
    </div>
</template>

<style lang="scss" scoped>
    .card{
        background-color: red;
        width: calc(100% / 4);
        & img{
            width: 100px;
            &:nth-child(1){
                background-color: black;
            }
        }
        & h5{
            font-weight: bolder;
        }
        &:nth-child(2n){
            align-self: flex-end;
        }
    }
</style>