<script>
    export default {
        name: 'UpcomingEvents',
        data(){
            return{
                eventsList: [
                    {
                        img: 'artist-event-04-250x300.jpg',
                        date: 'NOV 22, 2020',
                        title: 'Storytelling Workshop',
                        place: 'Texas, US'
                    },
                    {
                        img: 'artist-event-03-250x300.jpg',
                        date: 'OCT 10, 2020',
                        title: 'Painting Art Contest 2020',
                        place: 'New York, US'
                    },
                    {
                        img: 'artist-event-02-250x300.jpg',
                        date: 'NOV 23, 2020',
                        title: 'International Art Fair 2020',
                        place: 'Hamburg, Germany'
                    },
                    {
                        img: 'artist-event-01-250x300.jpg',
                        date: 'DEC 15, 2020',
                        title: 'Street Performance: Call for Artist',
                        place: 'Illinois, US'
                    }
                ]
            }
        }
    }
</script>

<template>
    <section class="upcoming-events py-5">
        <div class="container">
            <div class="upcoming-events__title text-center">
                <h2 class="subtitle">Upcoming Events</h2>
                <h2>Let's Work Together</h2>
            </div>
            <div class="upcoming-events__cards">
                <div class="event-card my-5" v-for="event in eventsList">
                    <div class="event-card__img">
                        <img :src="`/src/assets/upcomingEvents/${event.img}`" alt="">
                    </div>
                    <div class="event-card__info">
                        <div class="date">{{event.date}}</div>
                        <h5 class="mt-2 mb-3">{{event.title}}</h5>
                        <small><i class="fa-solid fa-location-dot"></i>{{event.place}}</small>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

    <style lang="scss" scoped>
    .upcoming-events{
        position: relative;
        overflow: hidden;
        .upcoming-events__cards{
            display: flex;
            flex-wrap: wrap;
            &::before{
                content: "";
                display: inline-block;
                width: 100%;
                height: 100%;
                background-image: url('/src/assets/upcomingEvents/artist-shape-02.png');
                background-repeat: no-repeat;
                position: absolute;
                left: -370px;
                bottom: -320px;
                transform: rotate(-80deg);
            }
            &::after{
                content: "";
                display: inline-block;
                width: 400px;
                height: 100px;
                background-image: url('/src/assets/upcomingEvents/events.png');
                background-repeat: no-repeat;
                background-position: center;
                position: absolute;
                left: -150px;
                bottom: 200px;
                transform: rotate(90deg);
                color: #f4ebe2;
            }
            .event-card{
                width: calc(100% / 2);
                display: flex;
                align-items: center;
                z-index: 10;
                &:hover img{
                    filter: drop-shadow(0 0 5px orange);
                }
                &:hover .event-card__info{
                    margin-left: 40px;
                    opacity: 1;
                }
                &:nth-child(2)::before{
                    content: "";
                    display: inline-block;
                    position: absolute;
                    right: 30px;
                    top: 90px;
                    width: 150px;
                    height: 150px;
                    background-image: url('/src/assets/upcomingEvents/maxcoach-shape-13-96x96.png');
                    background-repeat: no-repeat;
                    transform: rotate(10deg);
                }
                &:nth-child(2)::after{
                    content: "";
                    display: inline-block;
                    position: absolute;
                    right: 0;
                    top: 100px;
                    width: 300px;
                    height: 300px;
                    background-image: url('/src/assets/upcomingEvents/artist-shape-01-300x288.png');
                    background-repeat: no-repeat;
                    transform: rotate(10deg);
                }
                &:nth-child(3), &:nth-child(4){
                    text-align: right;
                    &:hover .event-card__info{
                        left: -200px;
                    }
                    .event-card__img img{
                        position: relative;
                        right: -380px;
                    }
                    .event-card__info{
                        position: relative;
                        left: 355px;
                    }
                }
                &:nth-child(4){
                    &:hover .event-card__info{
                        left: -270px;
                    }
                }
                & .event-card__info{
                    margin-left: -230px;
                    transition: all 0.5s;
                    opacity: 0;
                    z-index: -1;
                    & .date{
                        color: #8c8c8c;
                    }
                    & h5{
                        font-weight: bolder;
                    }
                    & i{
                        margin-right: 5px;
                    }
                }
            }
        }
    }
</style>