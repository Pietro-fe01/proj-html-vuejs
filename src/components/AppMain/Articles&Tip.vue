<script>
export default {
    name: 'ArticlesTip'
}
</script>

<template>
    <section class="articles-tip py-5">
        <div class="container">
            <div class="articles-tip__title text-center pb-5">
                <h2 class="subtitle">Articles and Tips</h2>
                <h2>Latest From The Blog</h2>
            </div>
            <div class="articles-tip__container pb-5">
                <!-- Aside left -->
                <div class="aside-card left">
                    <img src="/src/assets/articlesTip/120084500_197897808368764_8114555493043279565_n.jpg" alt="">
                    <div class="aside-card__info">
                        <small class="card-role">ARTIST</small>
                        <h6 class="my-3">Brush Strokes Energize Trees in Paintings</h6>
                        <div class="card-details pb-3">
                            <small class="date">
                                <i class="fa-regular fa-calendar"></i> May 15, 2020
                            </small>
                            <small class="views">
                                <i class="fa-regular fa-eye"></i> 688 views
                            </small>
                        </div>
                    </div>
                </div>

                <!-- Middle -->
                <div class="middle-card">
                    <div class="bg">
                        <img src="/src/assets/articlesTip/artist-blog-02-500x680.jpg" alt="">
                    </div>
                    <div class="card-details">
                        <small class="card-role">ARTIST</small>
                        <h3 class="my-3">Connection Between Self- Portraits and Identity</h3>
                        <i class="me-3 fa-regular fa-calendar"></i> May 15, 2020
                        <i class="fa-regular fa-eye"></i> 397 views
                    </div>
                </div>

                <!-- Aside left -->
                <div class="aside-card right">
                    <img src="/src/assets/articlesTip/artist-blog-01-480x356.jpg" alt="">
                    <div class="aside-card__info">
                        <small class="card-role">ARTIST</small>
                        <h6 class="my-3">Pocket-Sized Notebooks Hold Miniature Paintings</h6>
                        <div class="card-details pb-3">
                            <small class="date">
                                <i class="fa-regular fa-calendar"></i> May 15, 2020
                            </small>
                            <small class="views">
                                <i class="fa-regular fa-eye"></i> 603 views
                            </small>
                        </div>
                    </div>
                </div>
            </div>
            <div class="out-link pt-5">
                <span>Get into details now? </span>
                <a href="#">View all posts &#8594</a>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .articles-tip{
        background-color: #f5f7fa;
        overflow: hidden;
        position: relative;
        &::before{
            content: "";
            display: block;
            width: 150%;
            height: 100%;
            position: absolute;
            top: 280px;
            left: -200px;
            background-image: url("/src/assets/articlesTip/maxcoach-shape-14.png");
            background-repeat: no-repeat;
            filter: contrast(0.5);
        }
        & .articles-tip__container{
            display: flex;
            justify-content: space-between;
            & .aside-card{
                width: 280px;
                height: 200px;
                &.left{
                    position: relative;
                    top: 170px;
                    &::before{
                        content: "";
                        display: inline-block;
                        width: 65px;
                        height: 65px;
                        background-color: transparent;
                        border-radius: 50%;
                        border: 9px solid #ecc5ab;
                        position: absolute;
                        top: -140px;
                        left: 10px;
                    }
                }
                &.right{
                    position: relative;
                    top: 55px;
                }
                & img{
                    width: 280px;
                    height: 200px;
                }
                &__info{
                    padding: 15px;
                    background-color: white;
                    & .card-role{
                        color: #9b89a2;
                    }
                    & h6{
                        font-weight: bolder;
                    }
                    & .card-details{
                        display: flex;
                        justify-content: space-between;
                        color: #7e7e7e;
                    }
                }
            }
            & .middle-card{
                width: 500px;
                height: 640px;
                position: relative;
                display: flex;
                &::before{
                    content: "";
                    display: inline-block;
                    width: 100px;
                    height: 100px;
                    background-image: url('/src/assets/articlesTip/maxcoach-shape-05.png');
                    position: absolute;
                    top: -35px;
                    left: -35px;
                }
                & .bg{
                    position: absolute;
                }
                & .card-details{
                    align-self: flex-end;
                    color: white;
                    font-weight: bolder;
                    padding: 50px 30px;
                    z-index: 2;
                    & h3{
                        font-size: 2.1875rem;
                    }
                }
            }
        }
        & .out-link{
            color: #8c8ba5;
            font-weight: bolder;
            text-align: center;
            & a{
                color: #ef6f31;
                text-decoration: none;
                position: relative;
                padding-bottom: 1px;
                &::after{
                    content: "";
                    display: inline-block;
                    position: absolute;
                    bottom: 0;
                    left: 0;
                    width: 100%;
                    height: 1.5px;
                    background-color: #e0e0e0;
                }
                &:hover::after{
                    background-color: #ef6f31;
                }
            }
        }
    }
</style>