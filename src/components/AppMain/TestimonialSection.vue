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
                    testimonialTitle: 'Hight level and quality',
                    testimonialDescription: 'descrizione quarta card',
                    testimonialImage: 'artist-testimonial-avatar-03.jpg',
                    testimonialName: 'Nome quarta card',
                    testimonialRole: 'Ruolo quarta card'
                },
            ],
            currentIndex: 1,
            effect: false
        }
    },
    methods: {
        changeIndex(data){
            return this.currentIndex = data;
        },
        prevContent(){
            if(this.currentIndex === 0){
                return this.testimonialList.length - 1;
            } else {
                return this.currentIndex - 1;
            }
        },
        nextContent(){
            if(this.currentIndex < this.testimonialList.length - 1){
                return this.currentIndex + 1;
            } else {
                return 0;
            }
        },
        changeSlides(direction){
            if(direction === 'prev'){
                if(this.currentIndex === 0){
                    this.currentIndex = this.testimonialList.length - 1;
                } else {
                    this.currentIndex--;
                }
            }
            if(direction === 'next'){
                this.effect = true;
                if(this.currentIndex === this.testimonialList.length - 1){
                    this.currentIndex = 0;
                } else {
                    this.currentIndex++;
                }
            }
        }
    }
}
</script>

<template>
    <section class="testimonials pt-5 pb-4">
        <div class="testimonials__title text-center">
            <h2 class="subtitle">Testimonials</h2>
            <h2 class="mb-5">Why do people love me?</h2>
        </div>
        <div class="ms-carousel">
            <button class="move-button prev" @click="changeSlides('prev')">
                <i class="fa-solid fa-circle-chevron-left"></i>
            </button>
            <!-- Card Sinistra -->
            <div class="carousel-card">
                <div class="carousel-card__description">
                    <h4 class="mb-4">{{this.testimonialList[this.prevContent()].testimonialTitle}}</h4>
                    <p class="mb-4">{{this.testimonialList[this.prevContent()].testimonialDescription}}</p>
                </div>
                <div class="carousel-card__profile">
                    <div class="profile__img">
                        <img :src="`/src/assets/testimonialSection/${this.testimonialList[this.prevContent()].testimonialImage}`" alt="">
                    </div>
                    <div class="profile__info">
                        <h6 class="name ms-4">{{this.testimonialList[this.prevContent()].testimonialName}}</h6>
                        <small class="role ms-4">{{this.testimonialList[this.prevContent()].testimonialRole}}</small>
                    </div>
                </div>
            </div>
            <!-- /Card Sinistra -->

            <!-- Card centro -->
            <div class="carousel-card active">
                <div class="carousel-card__description">
                    <h4 class="mb-4">{{this.testimonialList[this.currentIndex].testimonialTitle}}</h4>
                    <p class="mb-4">{{this.testimonialList[this.currentIndex].testimonialDescription}}</p>
                </div>
                <div class="carousel-card__profile">
                    <div class="profile__img">
                        <img :src="`/src/assets/testimonialSection/${this.testimonialList[this.currentIndex].testimonialImage}`" alt="">
                    </div>
                    <div class="profile__info">
                        <h6 class="name ms-4">{{this.testimonialList[this.currentIndex].testimonialName}}</h6>
                        <small class="role ms-4">{{this.testimonialList[this.currentIndex].testimonialRole}}</small>
                    </div>
                </div>
            </div>
            <!-- /Card centro -->

            <!-- Card destra -->
            <div class="carousel-card">
                <div class="carousel-card__description">
                    <h4 class="mb-4">{{this.testimonialList[this.nextContent()].testimonialTitle}}</h4>
                    <p class="mb-4">{{this.testimonialList[this.nextContent()].testimonialDescription}}</p>
                </div>
                <div class="carousel-card__profile">
                    <div class="profile__img">
                        <img :src="`/src/assets/testimonialSection/${this.testimonialList[this.nextContent()].testimonialImage}`" alt="">
                    </div>
                    <div class="profile__info">
                        <h6 class="name ms-4">{{this.testimonialList[this.nextContent()].testimonialName}}</h6>
                        <small class="role ms-4">{{this.testimonialList[this.nextContent()].testimonialRole}}</small>
                    </div>
                </div>
            </div>
            <!-- /Card destra -->
            <button class="move-button next" @click="changeSlides('next')">
                <i class="fa-solid fa-circle-chevron-right"></i>
            </button>
        </div>
        <ol class="carousel-moving p-0 m-0">
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
            position: relative;
            & .carousel-card{
                width: 450px;
                padding: 40px;
                background-color: white;
                font-size: 14px;
                opacity: 0.3;
                &.active{
                    opacity: 1;
                }
                & .carousel-card__description h4{
                    font-size: 20px;
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
        & .move-button{
            background-color: transparent;
            border: none;
            position: absolute;
            align-self: center;
            font-size: 30px;
            padding: 0;
            top: 50%;
            transform: translate(0, -50%);
            opacity: 0.3;
            &:hover{
                opacity: 1;
            }
            &.prev{
                left: 10px;
            }
            &.next{
                right: 10px;
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
                cursor: pointer;
                &.active{
                    background-color: black;
                    transform: scale(1.5);
                }
            }
        }
    }
</style>