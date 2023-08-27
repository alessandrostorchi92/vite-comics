<script>

export default {
    props: {
        thumb: String,
        series: String
    },

}

</script>

<template>

    <div class="card-container">
        
        <div class="card h-100 border-0">
            <img :src="thumb" class="card-img-top" alt="">
            <div class="card-body bg-dark text-white text-center d-flex flex-column mt-auto">
                {{ series.toUpperCase() }}
            </div>
        </div>

    </div>

</template>

<style lang="scss" scoped>
@use "../styles/partials/_variables.scss" as *;
@use "../styles/partials/mixins";

.card-container {
    display: flex;
}
.card-img-top {
    aspect-ratio: 1/1;
}
</style>