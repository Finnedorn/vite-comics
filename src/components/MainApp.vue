<template>
    <main class=" position-relative ">
        <div class="container-fluid top-main">
        </div>
        <div class="title-wrapper p-2 px-3 position-absolute ">
            <h4 class="font-my-light">
                CURRENT SERIES
            </h4>
        </div>
        <!--cards-->
        <div class="bg-my-dark">
            <div class="container py-5">
                <div class="d-flex flex-wrap  align-items-center justify-content-center py-3">
                    <div class="ms-4 pb-4" v-for="(cover,index) in comicsArr" :key="index">
                        <CardComponent :img="cover.thumb" :title="cover.series" />
                    </div>
                </div>
            </div>
        </div>
        <!--merchandise-->
        <div class="bg-my-light-blue">
            <div class="container py-5">
                <ul class="d-flex flex-wrap justify-content-evenly align-items-center align-content-center  ">
                    <li v-for="(el) in mainImgArr" class="me-4 py-4">
                        <a href="#" class="d-flex align-items-center justify-content-center">
                            <div class="img-wrapper">
                                <img :src="el.picture" :alt="el.info">
                            </div>
                            <h3 class="font-my-light fs-6 ms-3">{{el.title}}</h3>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </main>
</template>

<script>
import { comics } from '../data/dc-comics';
import CardComponent from './CardComponent.vue';
export default {
    name: 'MainApp',
    data() {
        return {
            comicsArr: comics,
            mainImgArr: [
                {
                    picture: "/img/buy-comics-digital-comics.png",
                    info: "buy-comics-digital-comics",
                    title: "DIGITAL COMICS"
                },
                {
                    picture: "/img/buy-comics-merchandise.png",
                    info: "buy-comics-merchandise",
                    title: "DC MERCHANDISE"
                },
                {
                    picture: "/img/buy-comics-subscriptions.png",
                    info: "buy-comics-subscriptions",
                    title: "SUBSCRIPTION"
                },
                {
                    picture: "/img/buy-comics-shop-locator.png",
                    info: "buy-comics-shop-locator",
                    title: "COMICS SHOP LOCATOR"
                },
                {
                    picture: "/img/buy-dc-power-visa.svg",
                    info: "buy-dc-power-visa",
                    title: "DC POWER VISA"
                }
            ],
        };
    },
    components: { CardComponent },
}
</script>

<style lang="scss" scoped>
.top-main {
    height: 420px;
    background-image: url(../../public/img/jumbotron.jpg);
    background-size: cover;
}

.title-wrapper {
    background-color: var(--light-blue);
    top: 395px;
    left: 185px;
}

h4 {
    font-size: 1.2rem;
    font-weight: bolder;
    transform: scale(1,1.2);
}
.img-wrapper {
    width: 50px;
    height: 50px;
}

ul>li:first-child>a>div {
    width: 40px;
    height: 40px;
    margin-bottom: 10px;
}

ul>li:nth-child(4)>a>div {
    width: 35px;
    height: 35px;
    margin-bottom: 20px;
}
</style>