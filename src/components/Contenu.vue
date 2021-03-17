<template>
  <div>
    <h1>Bienvenue</h1>
    <p>On va faire du VUE JS ici</p>
    <liste :prenom="name" :ville="village" :legacy="heritage"></liste>
    <!-- <liste :prenom="firstname"/> -->
  </div>
</template>

<script>
import Liste from "./Liste/Liste.vue";

export default {
  name: "Contenu",
  data() {
    return {
      name: ["Alexandre", "Andre", "Thomas"],
      village: "Compogne",
      heritage() {
        // console.log("hérité depuis contenu");
      },
    };
  },
  components: {
    liste: Liste,
  },
};
</script>

<style scoped>
h1 {
  text-decoration: underline;
}
</style>
