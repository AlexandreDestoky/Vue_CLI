<template>
  <div>
    <ul class="liste">
      <li v-for="(prenom, index) of tabPrenoms" v-bind:key="index">{{index}}.{{ prenom }} à réussi son examen</li>
    </ul>
    <p>{{ prenom[1] }}</p>
    <p>{{ reversing() }}</p>
    <p>{{legacy()}}</p>
    <p v-for="(prenom, index) of tabPrenoms" v-bind:key="index">{{presentation(prenom)}}</p>
    <button @click="test">Test</button>
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
    presentation(nom) {
      return `Salut ${nom} comment-vas tu ?`;
    },
    test() {
      console.log("test");
    }
  },
};
</script>

<style scoped src="./Liste.css"></style>
