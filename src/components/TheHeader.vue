<script>

export default {
    data() {
        return {
            navLinks: [
                { name: "CHARACTERS" },
                { name: "COMICS" },
                { name: "MOVIES" },
                { name: "TV" },
                { name: "GAMES" },
                { name: "COLLECTIBLES" },
                { name: "VIDEOS" },
                { name: "FANS" },
                { name: "NEWS" },
                { name: "SHOP" }
            ]
        }
    }

}

</script>

<template>
    <header>

        <div class="container d-flex justify-content-around justify-content-center align-items-center">

            <img src="../assets/img/dc-logo.png" alt="Logo DC">
            
            <ul class="nav nav-pills">
                <li class="nav-item" v-for="link in navLinks">
                    <a href="#" class="nav-link" v-bind:class="{'active': link.name === 'COMICS'}">{{ link.name }}</a>
                </li>
            </ul>

        </div>

    </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
</style>