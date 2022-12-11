<script>
    export default {
        name: 'MainFooter',
        data(){
            return{
                exploreMenu: [
                    {
                        label: 'Start here',
                        href: '#'
                    },
                    {
                        label: 'Success story',
                        href: '#'
                    },
                    {
                        label: 'Blog',
                        href: '#'
                    },
                    {
                        label: 'Courses',
                        href: '#'
                    },
                    {
                        label: 'Contact us',
                        href: '#'
                    },
                ],
                informationMenu: [
                    {
                        label: 'Membership',
                        href: '#'
                    },
                    {
                        label: 'Purchase guide',
                        href: '#'
                    },
                    {
                        label: 'Privacy policy',
                        href: '#'
                    },
                    {
                        label: 'Terms of services',
                        href: '#'
                    },
                ]
            }
        }
    }
</script>

<template>
    <div class="main-footer container py-5 px-0">
        <div class="agency">
            <!-- Address -->
            <div class="agency__address">
                <h5 class="mb-3">Address</h5>
                <small class="street">382 NE 191st # 87394 Miami, FL 33179-3899</small>
                <small class="number">+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)</small>
                <small class="email">support@maxcoach.com</small>
            </div>
            
            <!-- Social -->
            <div class="agency__social mt-4">
                <a href="#">
                    <i class="fa-brands fa-square-facebook"></i>
                </a>
                <a href="#">
                    <i class="fa-brands fa-twitter"></i>
                </a>
                <a href="#">
                    <i class="fa-brands fa-instagram"></i>
                </a>
                <a href="#">
                    <i class="fa-brands fa-linkedin"></i>
                </a>
            </div>
        </div>

        <!-- Menu Explore -->
        <nav class="menu-links">
            <ul class="">
                <h5 class="mb-3">Explore</h5>
                <li v-for="link in exploreMenu" class="mb-2"><a :href="link.href">{{link.label}}</a></li>
            </ul>
        </nav>

        <!-- Menu Information -->
        <nav class="menu-links">
            <ul class="">
                <h5 class="mb-3">Information</h5>
                <li v-for="link in informationMenu" class="mb-2"><a :href="link.href">{{link.label}}</a></li>
            </ul>
        </nav>

        <!-- Instagram section -->
        <div class="instagram">
            <div class="instagram__title">
                <h5 class="me-2">Instagram</h5>
                <a href="#">@maxcoach</a>
            </div>
            <div class="instagram__images mt-3">
                <img src="/src/assets/mainFooter/120084500_197897808368764_8114555493043279565_n.jpg" alt="">
                <img src="/src/assets/mainFooter/120012142_177596140500760_8623485824101406058_n.jpg" alt="">
                <img src="/src/assets/mainFooter/120099363_364334431619755_7198812647386067017_n.jpg" alt="">
            </div>
        </div>
    </div>
    <div class="main-footer__bottom pb-4">
        <!-- Copyright -->
        <div class="copyright">
            <small>&#169; 2020 Maxcoach. All Rights Reserved</small>
        </div>
    
        <!-- Link per tornare a inizio pagina -->
        <a href="#top" id="moving-top">
            <i class="fa-solid fa-arrow-up"></i>
        </a>
    </div>
</template>

<style lang="scss" scoped> 
    .main-footer{
        display: flex;
        flex-wrap: wrap;
        color: #696969;
        & h5{
            font-weight: bolder;
            color: black;
        }
        & .agency__address small{
            display: block;
            margin-bottom: 5px;
        }
        & .agency__social a{
            color: #b4b4b4;
            & i{
                font-size: 25px;
                transition: transform 0.5s;
                &:hover{
                    transform: scale(1.3);
                    filter: drop-shadow(0 0 5px #ef6f31);
                }
            }
        }
        & .menu-links{
            display: flex;
            & ul{
                list-style: none;
                & li a{
                    color: #696969;
                    text-decoration: none;
                    &:hover{
                        text-decoration: underline;
                    }
                }
            }
        }
        & .instagram{
            &__title{
                & h5{
                    display: inline-block;
                }
                & a{
                    color: #ef6f37;
                    text-decoration: none;
                }
            }
            &__images{
                & img{
                    width: 130px;
                    height: 130px;
                    margin-right: 25px;
                    transition: all 0.5s;
                    &:hover{
                        rotate: 360deg;
                        transform: scale(1.3);
                    }
                }
            }
        }
    }
    .main-footer__bottom{
        position: relative;
        .copyright{
            color: #696969;
            text-align: center;
        }
        #moving-top{
            position: absolute;
            right: 20px;
            bottom: 20px;
            background-color: #ef6f31;
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            text-align: center;
            line-height: 50px;
        }
    }

    /*--------------------
        RESPONSIVE
    --------------------*/
    @media screen and (min-width: 576px) {
        .main-footer{
            justify-content: space-around;
            & .agency{
                width: 100%;
                text-align: center;
                margin-bottom: 30px;
                &__social a{
                    margin: 0 15px;
                }
            }
        }
    }

    @media screen and (min-width: 768px) {
        .main-footer{
            justify-content: space-between;
            & .agency{
                width: auto;
                text-align: left;
                margin-bottom: 0;
                &__social a{
                    margin: 0;
                    margin-right: 30px;
                }
            }
        }
    }

    @media screen and (min-width: 1200px) {
        .main-footer{
            gap: 10px;
        }
    }
</style>