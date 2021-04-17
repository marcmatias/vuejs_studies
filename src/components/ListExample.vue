<template>
  <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
  <h2 v-for="name in fullNames" :key="name.first">
    {{ name.first }} {{ name.last }}
  </h2>
  <div v-for="actor in actors" :key="actor.name">
    <h2>{{ actor.name }}</h2>
    <h3 v-for="movie in actor.movies" :key="movie">{{ movie }}</h3>
  </div>
  <h2 v-for="(el, key, index) in myInfo" :key="el">
    {{ index }} {{ key }} : {{ el }}
  </h2>
  <!-- 
    Exemplo de geração de lista separando-os
    com hr, porém, sem resquicio do elemento 
    pai.
    -->
  <template v-for="name in names" :key="name">
    <h2>{{ name }}</h2>
    <hr />
  </template>
</template>

<script>
export default {
  name: "ListExample",
  data() {
    return {
      names: ["Bruce", "Clark", "Diana"],
      fullNames: [
        { first: "Bruce", last: "Wayne" },
        { first: "Clark", last: "Kent" },
        { first: "Princess", last: "Diana" },
      ],
      actors: [
        {
          name: "Christian Bale",
          movies: ["Batman", "The Prestige"],
        },
        {
          name: "Di Caprio",
          movies: ["Titanic", "Inception"],
        },
      ],
      myInfo: {
        name: "Marcel Marques",
        nick: "@marcmatias",
        work: "Software Developer",
      },
    };
  },
};
</script>

<style>
</style>