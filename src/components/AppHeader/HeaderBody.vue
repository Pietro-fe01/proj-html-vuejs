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
            ]
        }
    }
}
</script>

<template>
    <div class="container header-body">
        <div class="header-body__logo">
            <a href="#">
                <img src="/src/assets/dark-logo.png" alt="">
            </a>
        </div>
        <nav class="header-body__nav">
            <ul class="p-0 m-0">
                <li v-for="link in menuLinks">
                    <a :href="link.href">{{link.menuLabel}} <i class="fa-solid fa-chevron-down"></i></a>
                </li>
            </ul>
        </nav>
        <div class="header-body__social">
            <a href="#">
                <i class="fa-brands fa-twitter"></i>
            </a>
            <i class="fa-brands fa-facebook-f"></i>
            <i class="fa-brands fa-instagram"></i>
            <i class="fa-brands fa-linkedin"></i>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .container.header-body{
        display: flex;
        justify-content: space-between;
        align-items: center;
        & .header-body__logo img{
            width: 160px;
        } 
        & .header-body__nav ul{
            list-style: none;
            display: flex;
            & li{
                margin: 0 15px;
                padding: 30px 0;
                & a{
                    text-decoration: none;
                    color: #333333;
                    & .fa-chevron-down{
                        font-size: 9px;
                    }
                }
            }
        }
        & .header-body__social i{
            margin-left: 15px;
            color: #696969;
        }
    }
</style>