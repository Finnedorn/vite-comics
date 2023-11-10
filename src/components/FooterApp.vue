<template>
    <footer>
        <div class=" top-footer-wrapper position-relative  overflow-hidden">
            <div class="container">
                <div class="bg-logo-wrapper position-absolute ">
                    <img src="/public/img/dc-logo-bg.png " alt="dc-logo-bg">
                </div>
                <div class=" row-cols-6 d-flex py-5 ">
                    <!--col1-->
                    <div>
                        <ul>
                            <h5 class="font-my-light footer-title">
                                DC COMICS
                            </h5>
                            <li v-for="(el) in dcComicsArr" :key="el" >
                                <a href="#" class="font-my-grey footer-links">
                                    {{el}}
                                </a>
                            </li>
                        </ul>
                        <ul>
                            <h5 class="font-my-light footer-title">
                                SHOP
                            </h5>
                            <li v-for="(el) in shopArr" :key="el" >
                                <a href="#" class="font-my-grey footer-links">
                                    {{el}}
                                </a>
                            </li>
                        </ul>
                    </div>
                    <!--col2-->
                    <div>
                        <ul>
                            <h5 class="font-my-light footer-title">
                                DC
                            </h5>
                            <li v-for="(el) in dcArr" :key="el" >
                                <a href="#" class="font-my-grey footer-links">
                                    {{el}}
                                </a>
                            </li>
                        </ul>
                    </div>
                    <!--col3-->
                    <div>
                        <ul>
                            <h5 class="font-my-light footer-title">
                                SITES
                            </h5>
                            <li v-for="(el) in sitesArr" :key="el" >
                                <a href="#" class="font-my-grey footer-links">
                                    {{el}}
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
        <div class="bg-my-dark-grey py-4">
            <div class="container d-flex  justify-content-between align-items-center">
                <div class="ps-4">
                    <button type="button" class="btn btn-outline-primary font-my-light p-3">
                        SIGN-UP NOW!
                    </button>
                </div>
                <div>
                    <ul class="d-flex flex-row flex-wrap justify-content-between align-items-center">
                        <h5 class="footer-title font-my-light-blue pt-2">
                            FOLLOW US
                        </h5>
                        <li v-for="(el) in iconsArr" :key="el" class=" ms-3 ">
                            <a href="#" class="icon-wrapper">
                                <img :src="el.picture" :alt="el.info">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'FooterApp',
    data() {
        return {
            dcComicsArr: [
                'Characters',
                'Comics',
                'Movies',
                'TV',
                'Games',
                'Videos',
                'News'
            ],
            shopArr: [
                'Shop DC',
                'Shop DC Collectibles'
            ],
            dcArr: [
                'Terms Of Use',
                'Privacy policy (new)',
                'Ad Choices',
                'Advertising',
                'Jobs',
                'Subscriptions',
                'Talent Workshop',
                'CPSC Certificates',
                'Ratings',
                'Shop Help',
                'Contact Us'
            ],
            sitesArr: [
                "DC",
                "MAD Magazine",
                "DC Kids",
                "DC Universe",
                "DC Power Visa"
            ],
            iconsArr: [
                {
                    picture: "/img/footer-facebook.png",
                    info: "footer-facebook.png"
                },
                {
                    picture: "/img/footer-periscope.png",
                    info: "footer-periscope.png"
                },
                {
                    picture: "/img/footer-pinterest.png",
                    info: "footer-pinterest.png"
                },
                {
                    picture: "/img/footer-twitter.png",
                    info: "footer-twitter.png"
                },
                {
                    picture: "/img/footer-youtube.png",
                    info: "footer-youtube.png"
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.top-footer-wrapper {
    width: 100%;
    height: 400px;
    background-image: url('/img/footer-bg.jpg');
    background-size: cover;
}

.footer-title {
    font-size: 1.1rem;
    font-weight: bolder;
    transform: scale(1,1.2);
}
.footer-links {
    font-size: 0.8rem;
}

.bg-logo-wrapper {
    right: 180px;
    bottom: -80px;
}

.btn-outline-primary {
    --bs-btn-border-color: var(--light-blue);
}

.btn {
    border-radius: none !important;
    border: 2px solid var(--light-blue) !important;
}

.font-my-light-blue {
    color: var(--light-blue);
}

.icon-wrapper {
    width: 20px;
    height: 20px;
}

</style>