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
            transition: 0.3s ease-out;
            bottom: 0; left: 0; right: 0; 
            height: 0%; width: 100%;
        }
        & span {         
            position: relative;
        }
        &:hover{
            color: white !important;
            &::before{
                height: 100%;
            }
        }
    }
</style>