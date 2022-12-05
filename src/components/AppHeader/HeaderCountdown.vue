<script>
import CommonButton from '../common/CommonButton.vue'
export default {
    name: 'HeaderCountdown',
    components: {
        CommonButton
    }
}
</script>

<template>
    <div class="header-countdown">
        <p class="m-0">Starts TOMORROW! Our biggest event of the year...</p>
        <div class="timer">
            <i class="clock-icon fa-regular fa-clock"></i>
            <h5 class="m-0">00 : 00 : 00</h5>
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
            margin: 0 30px;
            & .clock-icon{
                margin-right: .5rem;
                transform: translate(0px, 1px);
            }
        }
        & .ticket-button{
            margin: .625rem 0;
        }
    }
</style>