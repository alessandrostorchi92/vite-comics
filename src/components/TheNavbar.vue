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

    <div class="container top-bar">

        <img src="../assets/img/dc-logo.png" alt="Logo DC">

        <ul class="nav nav-pills">
            <li class="nav-item" v-for="link in navLinks">
                <a href="#" class="nav-link" v-bind:class="{ 'link-active': link.name === 'COMICS' }">{{ link.name }}</a>
            </li>
        </ul>

    </div>

</template>


<style lang="scss" scoped>
@use "../styles/partials/_variables.scss" as *;
@use "../styles/partials/mixins";

.top-bar {
    @include mixins.flex-content;
    height: 120px;

    img {
        width: 80px;
    }
}

a {
    color: $color-secondary;
    font-weight: bolder;

    &.link-active {
        color: $color-primary;
        border-bottom: 3px solid $color-primary;
        border-radius: 0;
        
    }
}

</style>