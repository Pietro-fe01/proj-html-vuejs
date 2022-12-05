<script>
import HeaderCountdown from './HeaderCountdown.vue';
import HeaderBody from './HeaderBody.vue';

export default {
    name: 'AppHeader',
    components: {
        HeaderCountdown,
        HeaderBody
    }
}
</script>

<template>
    <header>
        <HeaderCountdown/>
        <HeaderBody/>
    </header>
</template>

<style lang="scss" scoped>
    header{
        position: sticky;
        top: 0;
        left: 0;
        right: 0;
        z-index: 100;
        background-color: white;
    }
</style>