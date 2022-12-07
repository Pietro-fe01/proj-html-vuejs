<script>
export default {
    name: 'CommonButton',
    props: {
        textButton: String,
    }
}
</script>

<template>
    <button>{{textButton}}</button>
</template>

<style lang="scss" scoped>
    button{
        background-color: #ef6f31;
        color: white;
        padding: .3125rem 1.875rem;
        border-radius: .3125rem;
        border: none;
        font-weight: bold;
        font-size: .8125rem;
        transition: background 0.4s;

        &:hover{
            background-color: #6ac5f1 !important;
            color: white !important;
        }
    }
</style>