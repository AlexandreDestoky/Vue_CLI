<template>
  <div>
    <h1>Bienvenue</h1>
    <p>On va faire du VUE JS ici</p>
    <liste :prenom="firstname"></liste>
    <!-- <liste :prenom="firstname"/> -->
  </div>
</template>

<script>
import Liste from "./Liste/Liste.vue";

export default {
  name: "Contenu",
  data() {
    return {
      firstname: "Alexandre",
    }
  },
  components: {
    "liste": Liste
  },
};
</script>

<style scoped>
  h1 {
    text-decoration: underline;
  }
</style>
