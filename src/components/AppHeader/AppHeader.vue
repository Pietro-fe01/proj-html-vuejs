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
</style>