<script>
import HeroSection from './HeroSection.vue';
import ArtistCoaching from './ArtistCoaching.vue';

export default {
    name: 'AppMain',
    components: {
        HeroSection,
        ArtistCoaching
    }
}
</script>

<template>
    <main>
        <HeroSection/>
        <ArtistCoaching/>
    </main>
</template>

<style lang="scss" scoped>
</style>