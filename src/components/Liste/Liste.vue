<template>
  <div>
    <ul class="liste">
      <li v-for="(prenom, index) of tabPrenoms" v-bind:key="index">{{index}}.{{ prenom }} à réussi son examen</li>
    </ul>
    <p>{{ prenom[1] }}</p>
    <p>{{ reversing() }}</p>
    <p>{{legacy()}}</p>
  </div>
</template>

<script>
export default {
  name: "Liste",
  data() {
    return {
      tabPrenoms: ["Jean", "Marc", "Julien", "Andre"],
    };
  },
  props: { 
    prenom: {
      type: Array
    }, 
    ville: {
      type: String
    },
    legacy: {
      type: Function
    }
   },
  methods: {
    reversing() {
      return this.ville
        .split("")
        .reverse()
        .join("");
    },
  },
};
</script>

<style scoped src="./Liste.css"></style>
