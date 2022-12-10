<script>
export default {
    name: 'CommonButton',
    props: {
        textButton: String,
    }
}
</script>

<template>
    <button class="ms-btn hover-slide-up">
        <span>{{textButton}}</span>
    </button>
</template>

<style lang="scss" scoped>
    ::before,
    ::after {
        position: absolute;
        content: "";
    }
    .ms-btn {
        background-color: #ef6f31;
        border-radius: .3125rem;
        border: none;
        font-weight: bolder;
        font-size: .8125rem;
        position: relative;
        color: white;
        &::before {
            background-color: #6ac5f1;
            border-radius: .3125rem;
            bottom: 0; left: 0;
            height: 100%; width: 0%;
            transition: 0.3s ease-out;
        }
        & span {         
            position: relative;
        }
        &:hover{
            color: white !important;
            &::before{
                width: 100%;
            }
        }
    }
</style>