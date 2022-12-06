<script>
import HeroSection from './HeroSection.vue';
import ArtistCoaching from './ArtistCoaching.vue';
import TestimonialSection from './TestimonialSection.vue';
import LatestCourses from './LatestCourses.vue';
import ArticlesTip from './Articles&Tip.vue';

export default {
    name: 'AppMain',
    components: {
        HeroSection,
        ArtistCoaching,
        TestimonialSection,
        LatestCourses,
        ArticlesTip
    }
}
</script>

<template>
    <main>
        <HeroSection/>
        <ArtistCoaching/>
        <TestimonialSection/>
        <LatestCourses/>
        <ArticlesTip/>
    </main>
</template>

<style lang="scss" scoped>
</style>