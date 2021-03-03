<template>
  <div>
    <h1>Bienvenue {{prenom}}</h1>
    <p>On va faire du VUE JS ici</p>
  </div>
</template>

<script>
export default {
  name: "Contenu",
  data() {
    return {
      prenom: "Alexandre"
    }
  }
};
</script>

<style scoped>
  h1 {
    text-decoration: underline;
  }
</style>
