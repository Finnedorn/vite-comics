<template>
    <main>
        <div class="bg-my-dark">
            <div class="container py-5">
                <h2 class="font-my-light">
                    (ﾉ◕ヮ◕)ﾉ*:･ﾟ✧ Content goes here
                </h2>
            </div>
        </div>
        <div class="bg-my-light-blue">
            <div class="container py-5">
                <ul class="d-flex flex-row flex-wrap justify-content-between align-items-center align-content-center  ">
                    <li v-for="(el) in mainImgArr" class="me-4">
                        <a href="#" class="text-decoration-none d-flex align-items-center justify-content-center">
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
export default {
    name: 'MainApp',
    data() {
        return {
            mainImgArr: [
                {
                    picture:"/public/img/buy-comics-digital-comics.png",
                    info:"buy-comics-digital-comics",
                    title:"DIGITAL COMICS"

                },
                {
                    picture:"/public/img/buy-comics-merchandise.png",
                    info:"buy-comics-merchandise",
                    title:"DC MERCHANDISE"
                },
                {
                    picture:"/public/img/buy-comics-subscriptions.png",
                    info:"buy-comics-subscriptions",
                    title:"SUBSCRIPTION"
                },
                {
                    picture:"/public/img/buy-comics-shop-locator.png",
                    info:"buy-comics-shop-locator",
                    title:"COMICS SHOP LOCATOR"
                },
                {
                    picture: "/public/img/buy-dc-power-visa.svg",
                    info:"buy-dc-power-visa",
                    title:"DC POWER VISA"
                }
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
.bg-my-dark {
    background-color: var(--dark);
}
.bg-my-light-blue {
    background-color: var(--light-blue);
}
.font-my-light {
    color: var(--light);
}

ul{
    list-style: none;
}

img {
    width: 100%;
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