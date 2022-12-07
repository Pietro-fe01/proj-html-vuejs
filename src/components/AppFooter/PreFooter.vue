<script>
    export default {
        name: 'PreFooter'
    }
</script>

<template>
    <div class="pre-footer">
        <div class="container">
            <div class="pre-footer__title me-5">
                <h4>Newsletter to get in touch</h4>
            </div>
            <form class="form-floating ms-5" @submit.prevent>
                <input type="email" class="form-control" id="floatingInput" placeholder="name@example.com">
                <label for="floatingInput">Your e-mail</label>
                <button type="submit">&#10141;</button>
            </form>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .pre-footer{
        background-color: #244186;
        color: white;
        padding: 50px 0;
        overflow: hidden;
        position: relative;
        &::before{
            content: "";
            display: inline-block;
            background-image: url('/src/assets/preFooter/artist-shape-color-paint-top-left-300x170.png');
            position: absolute;
            top: 0;
            left: 0;
            width: 300px;
            height: 170px;
        }
        &::after{
            content: "";
            display: inline-block;
            background-image: url('/src/assets/preFooter/artist-shape-color-paint-bottom-right-300x153.png');
            position: absolute;
            bottom: 0;
            right: 0;
            width: 300px;
            height: 153px;
        }
        & .container{
            display: flex;
            justify-content: center;
            & .pre-footer__title{
                width: 17%;
                & h4{
                    text-align: right;
                }
            }
            & .form-floating{
                width: 40%;
                & .form-control{
                    background-color: transparent;
                    border: none;
                    border-bottom: 1px solid #5b71a4;
                    color: white;
                    border-radius: 0;
                    padding: 30px 0 0 0;
                    position: relative;
                    &:focus{
                        box-shadow: none;
                    }
                }
                & label{
                    font-size: 20px;
                }
                & button{
                    border: none;
                    background-color: transparent;
                    color: white;
                    font-size: 35px;
                    position: absolute;
                    padding: 0;
                    margin: 0;
                    right: -15px;
                    top: 50%;
                    transform: translate(-50%, -50%);
                }
            }
        }
    }
</style>