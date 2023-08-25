<script>

import TheNavbar from "./TheNavbar.vue"
import TheHeroSection from "./TheHeroSection.vue"

export default {

    components: {
        TheNavbar,
        TheHeroSection
    },

}

</script>

<template>

        <TheNavbar></TheNavbar>
        <TheHeroSection></TheHeroSection>

</template>

<style lang="scss" scoped>

@use "../styles/partials/_variables.scss" as *;
@use "../styles/partials/mixins";

</style>