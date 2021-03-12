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
    <input type="checkbox" v-model="boule">
    <input type="date" v-model="anniversaire">
    <input type="email" v-model="monEmail">
    <input type="password" v-model="mdp">
    <input type="color" v-model="favColor">
  </div>
</template>

<script>
export default {
  name: "Liste",

  data() {
    return {
      monEmail: "adestoky@yahoo.fr",
      tabPrenoms: ["Jean", "Marc", "Julien", "Andre"],
      boule:true,
      anniversaire:"1997-02-05",
      mdp:"salut",
      favColor : "#c5e3b8"
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
