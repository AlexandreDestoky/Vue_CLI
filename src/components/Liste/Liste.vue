<template>
  <ul class="liste">
    <li v-for="(prenom,index) of tabPrenoms" v-bind:key="index">{{prenom}} à réussi son examen</li>
  </ul>
</template>


<script>
export default {
  name: "Liste",
  data() {
    return {
      tabPrenoms: ["Jean","Marc","Julien","Andre"]
    }
  }
}
</script>


<style scoped src="./Liste.css">

</style>