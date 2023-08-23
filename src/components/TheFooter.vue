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

        <!-- Prima sezione del footer  -->

        <div class="container">

            <!-- Sezione DC Comics e Shop  -->
            <div>

                <h5>DC COMICS</h5>
                <ul class="nav flex-column">
                    <li class="nav-item" v-for="link in DcComicsLinks">
                        <a class="nav-link" aria-current="page" href="#">{{ link.name }}</a>
                    </li>
                </ul>

                <h5>SHOP</h5>
                <ul class="nav flex-column">
                    <li class="nav-item" v-for="link in ShopLinks">
                        <a class="nav-link" aria-current="page" href="#">{{ link.name }}</a>
                    </li>
                </ul>

            </div>
            
            <!-- Sezione DC  -->
            <div>

                <h5>DC</h5>
                <ul class="nav flex-column">
                    <li class="nav-item" v-for="link in  DCLinks">
                        <a class="nav-link" aria-current="page" href="#">{{ link.name }}</a>
                    </li>
                </ul>

            </div>

            <!-- Sezione Sites  -->
            <div>

                <h5>SITES</h5>
                <ul class="nav flex-column">
                    <li class="nav-item" v-for="link in SiteLinks">
                        <a class="nav-link" aria-current="page" href="#">{{ link.name }}</a>
                    </li>
                </ul>

            </div>

            <!-- Immagine Logo  -->
            <img src="../assets/img/dc-logo-bg.png" alt="Immagine Logo">

        </div>

        <!-- Seconda sezione del footer  -->

        <div class="container">

            <div class="d-flex  justify-content-around justify-content-center align-items-center">

                <!-- Sezione di sinistra  -->

                <!-- Call to Action Sign Up -->
                <button type="button" class="btn border-primary border-2 p-2 fw-semibold fs-5">SIGN-UP NOW!</button>

                <!-- Sezione di destra  -->

                <div>

                    <!-- Call to Action Follow Us -->
                    <span class="fw-semibold fs-4">FOLLOW US</span>

                    <!-- Social Icons  -->

                    <!-- // Questa procedimento mi permette di stampare le immagini dinamicamente su vite-vue  -->
                    <div v-for="icon in SocialIcons">
                        <img :src="getImagePath(`../assets/img/${icon.img}`)" alt="">
                    </div>

                </div>

            </div>

        </div>

    </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/_variables.scss" as *;
</style>