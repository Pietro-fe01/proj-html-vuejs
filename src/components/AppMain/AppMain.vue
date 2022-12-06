<script>
import HeroSection from './HeroSection.vue';
import ArtistCoaching from './ArtistCoaching.vue';
import TestimonialSection from './TestimonialSection.vue';

export default {
    name: 'AppMain',
    components: {
        HeroSection,
        ArtistCoaching,
        TestimonialSection
    }
}
</script>

<template>
    <main>
        <HeroSection/>
        <ArtistCoaching/>
        <TestimonialSection/>
    </main>
</template>

<style lang="scss" scoped>
</style>