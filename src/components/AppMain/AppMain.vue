<script>
import HeroSection from './HeroSection.vue';
import ArtistCoaching from './ArtistCoaching.vue';
import TestimonialSection from './TestimonialSection.vue';
import LatestCourses from './LatestCourses.vue';
import ArticlesTip from './Articles&Tip.vue';
import UpcomingEvents from './UpcomingEvents.vue';

export default {
    name: 'AppMain',
    components: {
        HeroSection,
        ArtistCoaching,
        TestimonialSection,
        LatestCourses,
        ArticlesTip,
        UpcomingEvents
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
        <UpcomingEvents/>
    </main>
</template>

<style lang="scss" scoped>
    section{
        overflow: hidden;
    }
</style>