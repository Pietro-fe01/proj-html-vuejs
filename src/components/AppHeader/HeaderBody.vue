<script>
export default {
    name: 'HeaderBody',
    data(){
        return{
            menuLinks: [
                {
                    menuLabel: 'Home',
                    href: '#'
                },
                {
                    menuLabel: 'Pages',
                    href: '#'
                },
                {
                    menuLabel: 'Courses',
                    href: '#'
                },
                {
                    menuLabel: 'Features',
                    href: '#'
                },
                {
                    menuLabel: 'Blog',
                    href: '#'
                },
                {
                    menuLabel: 'Shop',
                    href: '#'
                }
            ],
            clicked: false
        }
    }
}
</script>

<template>
    <div class="container header-body">
        <div class="header-body__logo">
            <a href="#">
                <img src="/src/assets/appHeader/dark-logo.png" alt="">
            </a>
            <!-- Menu che appare solo da mobile -->
            <nav class="mobile-menu d-lg-none ms-4">
                <i class="fa-solid fa-bars" @click="clicked = !clicked"></i>
                <!-- Al click dell'icona menu si aprono i link -->
                <div v-if="clicked" class="open-menu">
                    <nav>
                        <ul class="m-0 p-0">
                            <li v-for="link in menuLinks">
                                <a :href="link.href">{{link.menuLabel}}
                                    <i class="fa-solid fa-chevron-down"></i>
                                </a>
                            </li>
                        </ul>
                    </nav>
                </div>
            </nav>
            <!-- /Menu che appare solo da mobile -->
        </div>
        <nav class="header-body__nav d-none d-lg-block">
            <ul class="p-0 m-0">
                <li v-for="link in menuLinks">
                    <a :href="link.href">{{link.menuLabel}}
                        <i class="fa-solid fa-chevron-down"></i>
                    </a>
                </li>
            </ul>
        </nav>
        <div class="header-body__social">
            <a href="#">
                <i class="fa-brands fa-twitter"></i>
            </a>
            <a href="#">
                <i class="fa-brands fa-facebook-f"></i>
            </a>
            <a href="#">
                <i class="fa-brands fa-instagram"></i>
            </a>
            <a href="#">
                <i class="fa-brands fa-linkedin"></i>
            </a>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .container.header-body{
        display: flex;
        justify-content: space-between;
        align-items: center;
        min-height: 80px;
        & .header-body__logo{
            display: flex;
            align-items: flex-end;
            & img{
                width: 10rem;
            }
            & .mobile-menu{
                position: relative;
                & i{
                    cursor: pointer;
                }
                & .open-menu{
                    position: absolute;
                    top: 30px;
                    left: 0;
                    border-radius: 10px;
                    background-color: white;
                    border: 1px solid black;
                    & nav ul{
                        list-style: none;
                        & li{
                            padding: 5px 15px;
                            &:first-child{
                                border-top-left-radius: 10px;
                                border-top-right-radius: 10px;
                            }
                            &:last-child{
                                border-bottom-left-radius: 10px;
                                border-bottom-right-radius: 10px;
                            }
                            & a{
                                text-decoration: none;
                                color: #333333;
                                display: flex;
                                align-items: center;
                                & i{
                                    font-size: 10px;
                                    margin-left: 5px;
                                    transition: transform 0.5s;
                                }
                            }
                            &:hover {
                                filter: drop-shadow(0 0 3px #ef6f31);
                                & i{
                                    transform: rotate(-90deg);
                                }
                            }
                        }
                    }
                }
            }
        } 
        & .header-body__nav ul{
            list-style: none;
            display: flex;
            & li{
                margin: 0 .9375rem;
                padding: 28px 0;
                & a{
                    text-decoration: none;
                    color: #333333;
                    display: flex;
                    align-items: center;
                    &:hover{
                        filter: drop-shadow(0 0 5px #ef6f31);
                        & i{
                            transform: rotate(180deg);
                        }
                    }
                }
                & .fa-chevron-down{
                    font-size: .5625rem;
                    margin-left: 5px;
                    transition: transform 0.5s;
                }
            }
        }
        & .header-body__social i{
            margin-left: 1.25rem;
            color: #696969;
            font-size: 1.25rem;
            transition: transform 0.5s;
            &:hover{
                transform: scale(1.5);
                filter: drop-shadow(0 0 5px #ef6f31);
            }
        }
    }
</style>