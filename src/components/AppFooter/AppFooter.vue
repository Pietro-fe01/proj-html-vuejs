<script>
    import PreFooter from './PreFooter.vue';
    import MainFooter from './MainFooter.vue';

    export default {
        name: 'AppFooter',
        components: {
            PreFooter,
            MainFooter
        }
    }
</script>

<template>
    <footer>
        <PreFooter/>
        <MainFooter/>
    </footer>
</template>

<style lang="scss" scoped>

</style>