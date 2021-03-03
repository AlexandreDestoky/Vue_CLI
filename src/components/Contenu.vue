<template>
  <div>
    <h1>Bienvenue {{prenom}}</h1>
    <p>On va faire du VUE JS ici</p>
    <liste/>
  </div>
</template>

<script>
import Liste from "./Liste.vue";

export default {
  name: "Contenu",
  data() {
    return {
      prenom: "Alexandre"
    }
  },
  components: {
    "liste": Liste
  }
};
</script>

<style scoped>
  h1 {
    text-decoration: underline;
  }
</style>
