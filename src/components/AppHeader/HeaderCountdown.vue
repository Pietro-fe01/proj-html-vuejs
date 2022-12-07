<script>
import CommonButton from '../common/CommonButton.vue'
export default {
    name: 'HeaderCountdown',
    components: {
        CommonButton
    },
    data(){
        return {
            finalCountDown: '',
            isTimerOff: false
        }
    },
    methods:{
        setCountDown(){
            let countDownDate = new Date("Dec 7, 2022 18:00:00").getTime();

            let now = new Date().getTime();
                
            let distance = countDownDate - now;
                
            let days = Math.floor(distance / (1000 * 60 * 60 * 24));
            let hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            let minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            let seconds = Math.floor((distance % (1000 * 60)) / 1000);

            if(distance > 0){
                this.finalCountDown = days + "d : " + hours + "h : " + minutes + "m : " + seconds + "s";
            } else {
                this.isTimerOff = true;
                this.finalCountDown = "TIMER TERMINATO !";
            }

            this.settingCounter;
            return this.finalCountDown
        }
    },
    computed: {
        settingCounter(){
            let x = setInterval(() => {
                this.setCountDown();
            }, 1000);

            if(this.isTimerOff){
                clearInterval(x);
            }
        }
    }
}
</script>

<template>
    <div class="header-countdown">
        <p class="m-0">Starts TOMORROW! Our biggest event of the year...</p>
        <div class="timer">
            <i class="clock-icon fa-regular fa-clock"></i>
            <!-- <h5 class="m-0">00 : 00 : 00</h5> -->
            <!-- <h5 class="m-0" id="demo"></h5> -->
            <h5 class="m-0">{{this.setCountDown()}}</h5>
        </div>
        <CommonButton class="ticket-button" textButton = "Get ticket"/>
    </div>
</template>

<style lang="scss" scoped>
    .header-countdown{
        background-color: var(--header-countdown-bg-color);
        display: flex;
        justify-content: center;
        align-items: center;
        & p{
            color: #7b7977;
        }
        & .timer{
            display: flex;
            align-items: center;
            margin: 0 1.875rem;
            & .clock-icon{
                margin-right: .5rem;
                transform: translate(0px, .0625rem);
            }
            & h5{
                font-weight: bold;
            }
        }
        & .ticket-button{
            margin: .625rem 0;
        }
    }
</style>