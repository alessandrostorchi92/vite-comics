<script>

export default {

}

</script>

<template>
    <div class="jumbotron">
        <img src="../assets/img/jumbotron.jpg" alt="immagine comics di copertina">
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/_variables.scss" as *;
@use "../styles/partials/mixins";

.jumbotron {
    height: 350px;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
    }

}

</style>