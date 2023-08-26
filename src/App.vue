<!-- Tolgo l'attributo "setup" dallo script -->
<!-- Inserisco export default {} -->
<!-- Tolgo l'attributo scoped dallo style  -->

<script>

// Importo i nomi dei componenti
import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";
import ComicCardsList from "./components/ComicCardsList.vue";

// Importo i dati contenuto nel file.json da inserire nella props
import dcComics from "./db/dc-comics.json";

export default {

  // Specifico che voglio utilizzare questi componenti, aggiungendo la chiave "components" con all'interno i nomi dei componenti importati

  components: {
    TheHeader,
    TheFooter,
    ComicCardsList,
  },

  // Copio l'array contenente i dati jason dentro il data 

  data() {
    return {
      dcComics,
    }
  }

  // Dopo aver fatto ciò possiamo utilizzarli all'interno del template
  // Infine, controllo se tutto funziona con l'inspector

}

</script>

<template>
  <TheHeader></TheHeader>

  <main>

    <!-- Quando voglio utilizzare il componente ComicCards devo passare questa lista collegando le props con il data() -->
    <ComicCardsList :cardsList="dcComics"></ComicCardsList>

  </main>

  <TheFooter></TheFooter>
</template>

<styl lang="scss">

</styl>
