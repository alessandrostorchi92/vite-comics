<script>

export default {
    data() {
        return {
            DcComicsLinks: [
                { name: "Characters" },
                { name: "Comics" },
                { name: "Movies" },
                { name: "Tv" },
                { name: "Games" },
                { name: "Videos" },
                { name: "News" }
            ],
            ShopLinks: [
                { name: "Shop DC" },
                { name: "Shop DC Collectibles" }
            ],
            DCLinks: [
                { name: "Terms of use" },
                { name: "Privacy Policy" },
                { name: "Ad Choices" },
                { name: "Advertising" },
                { name: "Jobs" },
                { name: "Subscriptions" },
                { name: "Talent Workshops" },
                { name: "CPSC Certificates" },
                { name: "Ratings" },
                { name: "Shop Help" },
                { name: "Contact Us" },
            ],
            SiteLinks: [
                { name: "DC" },
                { name: "MAD Magazine" },
                { name: "DC Kids" },
                { name: "DC Universe" },
                { name: "DC Power Visa" }
            ],
            SocialIcons: [
                { img: "footer-facebook.png" },
                { img: "footer-twitter.png" },
                { img: "footer-youtube.png" },
                { img: "footer-pinterest.png" },
                { img: "footer-periscope.png" }
            ]

        }
    },
    methods: {

        // Questa funzione serve per stampare le immagini dinamicamente su vite-vue 
        getImagePath: function (img) {
            return new URL(img, import.meta.url).href;
        }

    }

}

</script>

<template>
    <footer>

        <!-- Sezione footer top   -->

        <section class="section-footer-top">

            <div class="container">

                <div class="row d-flex justify-content-center align-items-center justify-content-between">

                    <div class="col-6 d-flex gap-4">

                        <!-- Sezione DC Comics e Shop  -->
                        <div>
                            <h5 class="title">DC COMICS</h5>
                            <ul class="nav flex-column">
                                <li class="nav-item" v-for="link in DcComicsLinks">
                                    <a class="nav-link" aria-current="page" href="#">{{ link.name }}</a>
                                </li>
                            </ul>

                            <h5 class="title mt-2">SHOP</h5>
                            <ul class="nav flex-column">
                                <li class="nav-item" v-for="link in ShopLinks">
                                    <a class="nav-link" aria-current="page" href="#">{{ link.name }}</a>
                                </li>
                            </ul>
                        </div>

                        <!-- Sezione DC  -->
                        <div>
                            <h5 class="title">DC</h5>
                            <ul class="nav flex-column">
                                <li class="nav-item" v-for="link in  DCLinks">
                                    <a class="nav-link" aria-current="page" href="#">{{ link.name }}</a>
                                </li>
                            </ul>
                        </div>

                        <!-- Sezione Sites  -->
                        <div>
                            <h5 class="title">SITES</h5>
                            <ul class="nav flex-column">
                                <li class="nav-item" v-for="link in SiteLinks">
                                    <a class="nav-link" aria-current="page" href="#">{{ link.name }}</a>
                                </li>
                            </ul>
                        </div>

                    </div>

                    <div class="col-6">

                        <div class="logo-container">

                            <!-- Immagine Logo  -->
                            <img src="../assets/img/dc-logo-bg.png" alt="Immagine Logo">

                        </div>


                    </div>

                </div>

            </div>

        </section>

        <!-- Sezione footer bottom  -->

        <section class="section-footer-bottom">

            <div class="container h-100">

                <div class="h-100 d-flex justify-content-center align-items-center justify-content-between">

                    <!-- Left Section  -->

                    <button type="button" class="btn border-primary border-2 p-2 fw-bold fs-5 text-white">SIGN-UP
                        NOW</button>

                    <!-- Right Section  -->

                    <div class="d-flex align-items-center gap-2">

                        <span class="fw-bold fs-5 text-white">FOLLOW US</span>

                        <!-- Questa procedimento mi permette di stampare le immagini dinamicamente su vite-vue  -->

                        <div v-for="icon in SocialIcons">
                            <img :src="getImagePath(`../assets/img/${icon.img}`)" alt="">
                        </div>

                    </div>

                </div>

            </div>

        </section>

    </footer>

</template>

<style lang="scss" scoped>
@use "../styles/partials/_variables.scss" as *;
@use "../styles/partials/mixins";

.section-footer-top {
    background: url("../assets/img/footer-bg.jpg");
    height: 500px;
    overflow: hidden;
}

.title {
    color: $color-text;
    font-size: 1rem;
    font-weight: bold;
}

a {
    color: #959595;
    white-space: nowrap;
    font-size: 0.8rem;
    padding: 0.2rem;
}

.section-footer-bottom {
    background-color: #303030;
    height: 100px;
}
</style>