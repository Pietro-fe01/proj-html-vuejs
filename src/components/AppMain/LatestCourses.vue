<script>
    import CommonButton from '../common/CommonButton.vue';

    export default {
        name: 'LatestCourses',
        components: {
            CommonButton
        },
        data(){
            return {
                courseCardList: [
                    {
                        image: 'artist-hero-image-02.jpg',
                        price: '$18.00',
                        title: 'The acrylic Painting Academy',
                        lessons: '4 Lessons',
                        students: '50 Students',
                    },
                    {
                        image: 'artist-course-07-480x480.jpg',
                        price: '$21.00',
                        title: 'Drawing and Shading: Complete Course',
                        lessons: '14 Lessons',
                        students: '50 Students',
                    },
                    {
                        image: 'artist-course-06-480x480.jpg',
                        price: '$19.00',
                        title: 'The Color Theory for Digital Artist',
                        lessons: '7 Lessons',
                        students: '50 Students',
                    },
                    {
                        image: 'artist-course-05-480x480.jpg',
                        price: '$35.00',
                        title: 'Ultimate Guide to Digital Sketching for Beginner',
                        lessons: '14 Lessons',
                        students: '50 Students',
                    },
                    {
                        image: 'artist-course-04-480x480.jpg',
                        price: '$19.00',
                        title: 'Portrait Drawing The Smart Way',
                        lessons: '2 Lessons',
                        students: '50 Students',
                    },
                    {
                        image: 'artist-course-03-480x480.jpg',
                        price: '$19.00',
                        title: 'Mastering Watercolor Painting from Beginner',
                        lessons: '9 Lessons',
                        students: '50 Students',
                    },
                    {
                        image: 'artist-course-02-480x480.jpg',
                        price: '$25.00',
                        title: 'The Art & Science of Drawing',
                        lessons: '4 Lessons',
                        students: '50 Students',
                    },
                    {
                        image: 'artist-course-01-480x480.jpg',
                        price: '$22.00',
                        title: 'The Colored Pencil Drawing Course',
                        lessons: '6 Lessons',
                        students: '50 Students',
                    }
                ]
            }
        }
    }
</script>

<template>
    <section class="latest-courses py-5 container">
        <div class="latest-courses__title text-center pb-5">
            <h2 class="subtitle">Artist Coaching</h2>
            <h2>Latest Online Courses</h2>
        </div>
        <div class="latest-courses__cards">
            <div class="course-card mb-5" v-for="course in courseCardList">
                <div class="course-card__img text-center">
                    <img :src="`/src/assets/latestCourses/${course.image}`" alt="">
                </div>
                <div class="course-card__info">
                    <small class="price">{{course.price}}</small>
                    <h5 class="my-3">{{course.title}}</h5>
                    <div class="bottom-infos">
                        <span>
                            <i class="fa-regular fa-file-lines"></i> {{course.lessons}}
                        </span>
                        <span>
                            <i class="fa-regular fa-user"></i> {{course.students}}
                        </span>
                    </div>
                </div>
            </div>
            <div class="m-auto">
                <CommonButton textButton="View all courses &#8594"/>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .latest-courses__cards{
        display: flex;
        flex-wrap: wrap;
        & .course-card{
            cursor: pointer;
            transition: transform 0.6s;
            &:hover{
                transform: scale(1.1);
                & .course-card__info{
                    border: 3px solid #ef6f31;
                    // margin: -30px 0 30px 11px;
                    position: relative;
                }
            }
            & .course-card__img{
                & img{
                    width: 300px;
                    height: 300px;
                }
            }
            & .course-card__info{
                padding: 20px 25px;
                border: 3px solid transparent;
                background-color: white;
                transition: margin 0.3s;
                & .price{
                    color: #ef6f31;
                    font-weight: bolder;
                }
                & h5 {
                    font-weight: bolder;
                    font-size: 1.1875rem;
                }
                & .bottom-infos{
                    display: flex;
                    justify-content: space-between;
                    font-size: 14px;
                    color: #696969;
                }
            }
        }
        & button{
            padding: 10px 30px;
            background-color: rgba(239, 111, 49, 0.2);
            color: #ef6f31;
        }
    }

    /*--------------------
        RESPONSIVE
    --------------------*/
    @media screen and (min-width: 576px) {
        .latest-courses__cards{
            justify-content: center;
            & .course-card{
                width: 100%;
                &:hover .course-card__info{
                    margin: -30px 0 30px 108px;
                }
                &__info{
                    margin-left: 100px;
                    width: 280px;
                }
            }
        }
    }

    @media screen and (min-width: 768px) {
        .latest-courses__cards{
            & .course-card{
                width: calc(100% / 2);
                &:hover .course-card__info{
                    margin: -30px 0 30px 24px;
                }
                &__info{
                    margin-left: 0px;
                }
            }
        }
    }

    @media screen and (min-width: 992px) {
        .latest-courses__cards{
            & .course-card{
                &:hover .course-card__info{
                    margin: -30px 0 30px 84px;
                }
                &__info{
                    margin-left: 60px;
                }
            }
        }
    }

    @media screen and (min-width: 1200px) {
        .latest-courses__cards{
            & .course-card{
                width: calc(100% / 3);
                &:hover .course-card__info{
                    margin: -30px 0 30px 35px;
                }
                &__info{
                    margin-left: 15px;
                }
            }
        }
    }

    @media screen and (min-width: 1400px) {
        .latest-courses__cards{
            & .course-card{
                width: calc(100% / 4);
                &:hover .course-card__info{
                    margin: -30px 0 30px 11px;
                }
                &__info{
                    margin-left: 0px;
                }
            }
        }
    }
</style>