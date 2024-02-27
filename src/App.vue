<template>
  <main>
    <header>
      <h2>Star Wars Characters</h2>
    </header>
    <div>
      <ul>
        <li v-for="{name,  species, img} in characters" :key="name">
          <h3>{{ name }}</h3>
          <p>{{ species }}</p>
          <img :src="img.src" :alt="img.alt">
        </li>
      </ul>
    </div>
  </main>
</template>

<script setup>
const characters = [
  {
    name: "Chewbacca",
    side: "Light",
    species: "Wookie",
    img: {
      src: "https://images.pexels.com/photos/3526020/pexels-photo-3526020.jpeg",
      alt: "Chewbacca on endor",
    },
  },
  {
    name: "Boba Fett",
    side: "Dark",
    species: "Clone Human",
    img: {
      src: "https://images.pexels.com/photos/1437218/pexels-photo-1437218.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1",
      alt: "Boba Fett at a bbq?",
    },
  },
  {
    name: "Grogu",
    side: "Light",
    species: "Whatever Yoda is?",
    img: {
      src: "https://images.pexels.com/photos/7829101/pexels-photo-7829101.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1",
      alt: "Grogu looking for snacks",
    },
  },
];
</script>

<style scoped>
img {
  width: 200px;
}
</style>
