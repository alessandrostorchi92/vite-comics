<script>

export default {
    props: {
        thumb: String,
        series: String
    },

}

</script>

<template>

    <div class="card h-100 border-0 text-white text-center d-flex flex-column ms-auto">
        <img :src="thumb" alt="">
        <div class="card-body bg-dark">
            {{ card.series }}
        </div>
    </div>

</template>

<style lang="scss" scoped>
@use "../styles/partials/_variables.scss" as *;
@use "../styles/partials/mixins";

.single-card {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>