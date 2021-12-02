<template>
    <div class="mt-5 pt-4 bg">
        <!-- Carousel -->
        <div id="demo" class="carousel slide" data-bs-ride="carousel">

            <!-- Indicators/dots -->
            <div class="carousel-indicators mb-0">
                <button type="button" class="active btn" data-bs-target="#demo" data-bs-slide-to="0"></button>
                <button type="button" class="btn" data-bs-target="#demo" data-bs-slide-to="1"></button>
                <button type="button" class="btn" data-bs-target="#demo" data-bs-slide-to="2"></button>
                <button type="button" class="btn" data-bs-target="#demo" data-bs-slide-to="3"></button>
            </div>

            <!-- The slideshow/carousel -->
            <div class="carousel-inner">
                <div class="carousel-item active">
                <img src="../../../assets/images/myjio/caroceil/carosuel_1.jpg" alt="Los Angeles" class="d-block w-100">
                </div>
                <div class="carousel-item">
                <img src="../../../assets/images/myjio/caroceil/carosucil_2.jpg" alt="Chicago" class="d-block w-100">
                </div>
                <div class="carousel-item">
                <img src="../../../assets/images/myjio/caroceil/INDvsNZ-App-Desktop_3.jpg" alt="New York" class="d-block w-100">
                </div>
                <div class="carousel-item">
                <img src="../../../assets/images/myjio/caroceil/App-page-desktop-banner-1440x500_4.jpg" alt="New York" class="d-block w-100">
                </div>
            </div>
        </div>
        <!-- card section -->
        <div class="d-flex justify-content-center py-5">
            <section class="contain">
                <h5 class="text-muted ps-3 pb-3">Life is Beautiful with Jio Apps</h5>
                <div class="row mx-auto">
                    <div class="col-lg-3 col-md-6 mb-3" v-for="card in cards" :key="card.id">
                        <card :card="card" :id="id" :title="title" :cardimg="cardimg" :text="text" :iconimg="iconimg" :img1="img1" :img2="img2" :img3="img3" v-bind:class="clr" />
                    </div>
                </div>
            </section>
        </div>
    </div>
</template>

<script>
import card from './card.vue'
export default {
    name: 'index',
    data() {
        return {
            cards:[
                {
                    id: 1,
                    cardimg: require('../../../assets/images/myjio/card/home-myjio-v5_904a06738a22262052d670a5f61174cf.jpg'),
                    iconimg: require('../../../assets/images/myjio/cardicons/myjio-logo-thumb-34x34-v2.png'),
                    title: 'MyJio',
                    text: 'For everything Jio.',
                    img1: require('../../../assets/images/myjio/cardicons/1App store.png'),
                    img2: require('../../../assets/images/myjio/cardicons/google-play-button-jiosecurity.png'),
                    clr: 'red'
                },
                {
                    id: 2,
                    cardimg: require('../../../assets/images/myjio/card/promo-banner.432x270.jpg'),
                    iconimg: require('../../../assets/images/myjio/cardicons/JioSaavn-Icon-30x30-12.png'),
                    title: 'JioSaavn',
                    text: 'All your music. Anytime. Anywhere.',
                    img1: require('../../../assets/images/myjio/cardicons/1App store.png'),
                    img2: require('../../../assets/images/myjio/cardicons/google-play-button-jiosecurity.png'),
                    img3: require('../../../assets/images/myjio/cardicons/go-to-desktop-js.png')
                },
                {
                    id: 3,
                    cardimg: require('../../../assets/images/myjio/card/JioPages-Thumbnail-landing-page.jpg'),
                    iconimg: require('../../../assets/images/myjio/cardicons/jio-pages-logo-34x34-sticky1.png'),
                    title: 'JioPages',
                    text: 'Faster, Safer and Simply Yours.',
                    img1: require('../../../assets/images/myjio/cardicons/google-play-button-jiosecurity.png'),
                },
                {
                    id: 4,
                    cardimg: require('../../../assets/images/myjio/card/App Landing promo banner.png'),
                    iconimg: require('../../../assets/images/myjio/cardicons/Jiomeet-Logo-v1.png'),
                    title: 'JioMeet',
                    text: 'Video Conferencing App.',
                    img1: require('../../../assets/images/myjio/cardicons/1App store.png'),
                    img2: require('../../../assets/images/myjio/cardicons/google-play-button-jiosecurity.png'),
                    img3: require('../../../assets/images/myjio/cardicons/browser-logo-jm.png')
                },
                {
                    id: 5,
                    cardimg: require('../../../assets/images/myjio/card/Mask Group 13.png'),
                    iconimg: require('../../../assets/images/myjio/cardicons/Group 30977.png'),
                    title: 'JioHome',
                    text: 'Enhancing your home experience',
                    img1: require('../../../assets/images/myjio/cardicons/1App store.png'),
                    img2: require('../../../assets/images/myjio/cardicons/google-play-button-jiosecurity.png'),
                    img3: require('../../../assets/images/myjio/cardicons/go-to-desktop-js.png')
                },
                {
                    id: 6,
                    cardimg: require('../../../assets/images/myjio/card/home-jio-play-v5.jpg'),
                    iconimg: require('../../../assets/images/myjio/cardicons/logo-jiotv-v5.png'),
                    title: 'JioTV',
                    text: 'Daily dose of entertainment.',
                    img1: require('../../../assets/images/myjio/cardicons/1App store.png'),
                    img2: require('../../../assets/images/myjio/cardicons/google-play-button-jiosecurity.png'),
                },
                {
                    id: 7,
                    cardimg: require('../../../assets/images/myjio/card/Collage_432x270(1).jpg'),
                    iconimg: require('../../../assets/images/myjio/cardicons/jio-cinema-app-logo-v5_5.png'),
                    title: 'JioCinema',
                    text: 'Movies, TV Shows, Music & more.',
                    img1: require('../../../assets/images/myjio/cardicons/1App store.png'),
                    img2: require('../../../assets/images/myjio/cardicons/google-play-button-jiosecurity.png'),
                    img3: require('../../../assets/images/myjio/cardicons/go-to-desktop-js.png'),
                },
                {
                    id: 8,
                    cardimg: require('../../../assets/images/myjio/card/jpl-thumbnail-landing-pg.png'),
                    iconimg: require('../../../assets/images/myjio/cardicons/jioposlite-logo.png'),
                    title: 'JioPOS Lite',
                    text: 'Earn by helping Jio Customer',
                    img1: require('../../../assets/images/myjio/cardicons/google-play-button-jiosecurity.png'),
                },
                {
                    id: 9,
                    cardimg: require('../../../assets/images/myjio/card/App-landing-page-banner.jpg'),
                    iconimg: require('../../../assets/images/myjio/cardicons/JioNews_AppIcon-thumbnail.png'),
                    title: 'JioNews',
                    text: 'Your News. Your Language.',
                    img1: require('../../../assets/images/myjio/cardicons/1App store.png'),
                    img2: require('../../../assets/images/myjio/cardicons/google-play-button-jiosecurity.png'),
                    img3: require('../../../assets/images/myjio/cardicons/go-to-desktop-js.png'),
                },
                {
                    id: 10,
                    cardimg: require('../../../assets/images/myjio/card/jio-chat-img2_a-12-21apr.jpg'),
                    iconimg: require('../../../assets/images/myjio/cardicons/jiochat-main-applogo-57x57.png'),
                    title: 'JioChat',
                    text: 'An efficient way to stay connected.',
                    img1: require('../../../assets/images/myjio/cardicons/1App store.png'),
                    img2: require('../../../assets/images/myjio/cardicons/google-play-button-jiosecurity.png')
                },
                {
                    id: 11,
                    cardimg: require('../../../assets/images/myjio/card/Jio.com_banner.jpg'),
                    iconimg: require('../../../assets/images/myjio/cardicons/jio-drive-logo-14.png'),
                    title: 'JioCloud',
                    text: 'Backup your files and contacts.',
                    img1: require('../../../assets/images/myjio/cardicons/1App store.png'),
                    img2: require('../../../assets/images/myjio/cardicons/google-play-button-jiosecurity.png'),
                    img3: require('../../../assets/images/myjio/cardicons/go-to-desktop-js.png')
                },
                {
                    id: 12,
                    cardimg: require('../../../assets/images/myjio/card/home-jiojoin-ver1.jpg'),
                    iconimg: require('../../../assets/images/myjio/cardicons/jiojion-applogo-57x57.png'),
                    title: 'JioCall',
                    text: 'Get VoLTE & RCS on any phone.',
                    img1: require('../../../assets/images/myjio/cardicons/1App store.png'),
                    img2: require('../../../assets/images/myjio/cardicons/google-play-button-jiosecurity.png'),
                },
                {
                    id: 13,
                    cardimg: require('../../../assets/images/myjio/card/home-jio-security-v5_78909aa345f6122cf3929ecf050db170434334.jpg'),
                    iconimg: require('../../../assets/images/myjio/cardicons/jiosecurity-1.png'),
                    title: 'JioSecurity',
                    text: 'Protect phone, secure data.',
                    img1: require('../../../assets/images/myjio/cardicons/1App store.png'),
                    img2: require('../../../assets/images/myjio/cardicons/google-play-button-jiosecurity.png'),
                },
                {
                    id: 14,
                    cardimg: require('../../../assets/images/myjio/card/jiohealthhub-aplandingv1.jpg'),
                    iconimg: require('../../../assets/images/myjio/cardicons/jiohealthlogo-57x57.png'),
                    title: 'JioHealthHub',
                    text: 'Access tests, doctors & reports.',
                    img1: require('../../../assets/images/myjio/cardicons/1App store.png'),
                    img2: require('../../../assets/images/myjio/cardicons/google-play-button-jiosecurity.png'),
                },
            ]
        }
    },
    components:{
        card
    }
}
</script>

<style lang="scss" scoped>
.clr {
    color: red;
}
.bg {
    background: #ECECEC
}
// carousel
.carousel-indicators {
    .btn {
        width: 10px;
        height: 10px;
        border-radius: 50% !important;
    }
    .active {
        width: 25px !important;
        border-radius: 46% !important;
        background-color: #2f65b0;
    }
}
// card
.contain {
    width: 95%;
}
</style>