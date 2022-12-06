<script>
export default {
    name: 'TestimonialSection',
    data(){
        return {
            testimonialList: [
                {
                    testimonialTitle: 'It\'s a choice of quality for people with sppecial needs',
                    testimonialDescription: 'I am very strict person so I require everything to be organized and neat. Then, I\'ll be able to make things right and shine. MaxCoach guys just got me.',
                    testimonialImage: 'artist-testimonial-avatar-02.jpg',
                    testimonialName: 'Florence Themes',
                    testimonialRole: '/ Multimedia Admin'
                },
                {
                    testimonialTitle: 'High level of efficiency and scientific teaching methods',
                    testimonialDescription: 'I am free to learn at my own space, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.',
                    testimonialImage: 'artist-testimonial-avatar-04.jpg',
                    testimonialName: 'Mina Hallace',
                    testimonialRole: '/ Freelancer'
                },
                {
                    testimonialTitle: 'Professional team of specialists and passionate mentors at reach',
                    testimonialDescription: 'I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.',
                    testimonialImage: 'artist-testimonial-avatar-01.jpg',
                    testimonialName: 'Madley Pondor',
                    testimonialRole: '/ It Specialist'
                },
                {
                    testimonialTitle: 'Titolo Quarta Card',
                    testimonialDescription: 'descrizione quarta card',
                    testimonialImage: 'artist-testimonial-avatar-03.jpg',
                    testimonialName: 'Nome quarta card',
                    testimonialRole: 'Ruolo quarta card'
                },
            ],
            currentIndex: 1
        }
    },
    methods: {
        changeIndex(data){
            return this.currentIndex = data
        }
    }
}
</script>

<template>
    <section class="testimonials py-5">
        <div class="testimonials__title text-center">
            <h2 class="subtitle">Testimonials</h2>
            <h2 class="mb-5">Why do people love me?</h2>
        </div>
        <div class="ms-carousel">
            <div class="carousel-card" :class="{active : index === this.currentIndex}" v-for="(testimonial, index) in testimonialList">
                <div class="carousel-card__description">
                    <h4 class="mb-4">{{testimonial.testimonialTitle}}</h4>
                    <p class="mb-4">{{testimonial.testimonialDescription}}</p>
                </div>
                <div class="carousel-card__profile">
                    <div class="profile__img">
                        <img :src="`/src/assets/testimonialSection/${testimonial.testimonialImage}`" alt="">
                    </div>
                    <div class="profile__info">
                        <h6 class="name ms-4">{{testimonial.testimonialName}}</h6>
                        <small class="role ms-4">{{testimonial.testimonialRole}}</small>
                    </div>
                </div>
            </div>
        </div>
        <ol class="carousel-moving p-0">
            <li :class="{active : this.currentIndex === 1}" @click="changeIndex(1)"></li>
            <li :class="{active : this.currentIndex === 2}" @click="changeIndex(2)"></li>
            <li :class="{active : this.currentIndex === 3}" @click="changeIndex(3)"></li>
            <li :class="{active : this.currentIndex === 0}" @click="changeIndex(0)"></li>
        </ol>
    </section>
</template>

<style lang="scss" scoped>
    .testimonials{
        background-color: #faf8f6;
        & .ms-carousel{
            display: flex;
            justify-content: space-between;
            padding: 0 50px;
            & .carousel-card{
                width: 450px;
                padding: 40px;
                background-color: white;
                font-size: 14px;
                opacity: 0.3;
                &:last-child{
                    display: none;
                }
                &.active{
                    opacity: 1;
                }
                & .carousel-card__description h4{
                    font-size: 1rem;
                    font-weight: bold;
                }
                & .carousel-card__profile{
                    display: flex;
                    align-items: center;
                    & .profile__img img{
                        width: 70px;
                        object-fit: cover;
                        border-radius: 50%;
                    }
                    & .profile__info .role{
                        color: #aaaaaa;
                    }
                }
            }
        }
        & .carousel-moving{
            list-style: none;
            display: flex;
            justify-content: center;
            & li{
                width: 9px;
                height: 9px;
                border-radius: 50%;
                background-color: #d8d8d8;
                margin: 30px 10px;
                &.active{
                    background-color: black;
                    transform: scale(1.5);
                }
            }
        }
    }
</style>