<!-- Tolgo l'attributo "setup" dallo script -->
<!-- Inserisco export default {} -->
<!-- Tolgo l'attributo scoped dallo style  -->

<script>

// Importo i nomi dei componenti

import TheHeader from "./components/TheHeader.vue"
import TheFooter from "./components/TheFooter.vue"

export default {

  // Specifico che voglio utilizzare questi componenti, aggiungendo la chiave "components" con all'interno i nomi dei componenti importati

  components: {
    TheHeader,
    TheFooter
  }

  // Dopo aver fatto ciò possiamo utilizzarli all'interno del template
  // Infine, controllo se tutto funziona con l'inspector

}

</script>

<template>
  <TheHeader></TheHeader>
  <TheFooter></TheFooter>
</template>

<style>

</style>
