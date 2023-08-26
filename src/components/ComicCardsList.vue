<script>

import SingleCard from "./SingleCard.vue";

export default {

    props: {

        cardsList: {
            type: Array,
            required: true
        },
    },

    components: {
        SingleCard,
    },

}

</script>

<template>

    <div class="cards-container">

        <div class="py-5 container">
    
            <div class="row row-cols-6 g-4">
                
                <SingleCard v-for="(card, i) in cardsList" :key="`card_${i}`" :thumb="card.thumb" :series="card.series"></SingleCard>
    
            </div>
    
        </div>

    </div>

</template>

<style lang="scss" scoped> 
@use "../styles/partials/_variables.scss" as *;
@use "../styles/partials/mixins";
</style>
