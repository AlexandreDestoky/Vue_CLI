<template>
<div>
  <ul class="liste">
    <li v-for="(prenom,index) of tabPrenoms" v-bind:key="index">{{prenom}} à réussi son examen</li>
  </ul>
  <p>{{prenom}}</p>
</div>
</template>


<script>
export default {
  name: "Liste",
  data() {
    return {
      tabPrenoms: ["Jean","Marc","Julien","Andre"]
    }
  },
  props: ["prenom"]
}
</script>


<style scoped src="./Liste.css">

</style>