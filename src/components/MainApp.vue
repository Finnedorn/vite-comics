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
                <ul>
                    <li v-for="(el) in mainImgArr" class="me-4">
                        <a href="#">
                            <img :src="el" alt="">
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
                "/public/img/buy-comics-digital-comics.png",
                '/public/img/buy-comics-merchandise.png',
                '/public/img/buy-comics-subscriptions.png',
                '/public/img/buy-comics-shop-locator.png'
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
</style>