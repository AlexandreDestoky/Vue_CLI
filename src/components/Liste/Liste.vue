<template>
  <div>
    <ul class="liste">
      <li v-for="(prenom, index) of tabPrenoms" v-bind:key="index">{{ index }}.{{ prenom }} à réussi son examen</li>
    </ul>
    <p>{{ prenom[1] }}</p>
    <p>{{ reversing() }}</p>
    <p>{{ legacy() }}</p>
    <p v-for="(prenom, index) of tabPrenoms" v-bind:key="index">{{ presentation(prenom) }}</p>
    <button @click="test">Test</button>
    <input type="checkbox" v-model="boule" />
    <input type="date" v-model="anniversaire" />
    <input type="email" v-model="monEmail" />
    <input type="password" v-model="mdp" />
    <input type="color" v-model="favColor" />
    <hr />
    <input type="text" v-model="recherche" />
    <input type="range" max="5" v-model="niveau" />
    <input type="week" v-model="semaine" />
    <input type="tel" pattern="[0-9]{10}" v-model="monNum" />

    <p>{{ affiche() }}</p>
  </div>
</template>

<script>
export default {
  name: "Liste",

  data() {
    return {
      monEmail: "adestoky@yahoo.fr",
      tabPrenoms: ["Jean", "Marc", "Julien", "Andre"],
      boule: true,
      anniversaire: "1997-02-05",
      mdp: "salut",
      favColor: "#c5e3b8",
      recherche: "",
      niveau: 4,
      semaine: "2018-W18",
      monNum: "0475573885",
    };
  },
  props: {
    prenom: {
      type: Array,
    },
    ville: {
      type: String,
    },
    legacy: {
      type: Function,
    },
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
    },
    affiche(recherche) {
      console.log("le mot écrit est : " + recherche);
    },
  },
  computed: {},
};
</script>

<style scoped src="./Liste.css"></style>
