<template lang="pug">
  #app
    hero
    features
    showcase
</template>

<script>
import Hero from './components/Hero'
import Features from './components/Features'
import Showcase from './components/Showcase'

export default {
  name: 'app',
  components: {
    Hero,
    Features,
    Showcase
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Pacifico');
@font-face {
    font-family: Novecentos;
    src: ('../assets/novecentos.woff');
}

p {
    font-size: 0.8rem;
}

li {
    list-style-type: none;
}

body {
    margin: 0;
}

#app {
    font-family: Novecentos, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
}
</style>
