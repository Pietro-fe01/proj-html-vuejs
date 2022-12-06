<script>
import HeroSection from './HeroSection.vue';
import ArtistCoaching from './ArtistCoaching.vue';
import TestimonialSection from './TestimonialSection.vue';
import LatestCourses from './LatestCourses.vue';

export default {
    name: 'AppMain',
    components: {
        HeroSection,
        ArtistCoaching,
        TestimonialSection,
        LatestCourses
    }
}
</script>

<template>
    <main>
        <HeroSection/>
        <ArtistCoaching/>
        <TestimonialSection/>
        <LatestCourses/>
    </main>
</template>

<style lang="scss" scoped>
</style>