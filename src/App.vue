<template lang="pug">
  #app
    hero
    features
    showcase
    testimonials
    pricing
    social
</template>

<script>
import Hero from './components/Hero'
import Features from './components/Features'
import Showcase from './components/Showcase'
import Testimonials from './components/Testimonials'
import Pricing from './components/Pricing'
import Social from './components/Social'

export default {
  name: 'app',
  components: {
    Hero,
    Features,
    Showcase,
    Testimonials,
    Pricing,
    Social
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Pacifico');
@font-face {
  font-family: Novecentos;
  src: url('./assets/novecentos.woff2') format('woff2'),
  url('./assets/novecentos.woff') format('woff');
}

* {
  box-sizing: border-box;
}

p {
  font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
  font-size: 0.8rem;
  line-height: 1.5rem;
  color: #848484;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: 'Myriad Pro', Helvetica, Arial, sans-serif;
  color: #222222;
}

li {
  list-style-type: none;
}

body {
  margin: 0;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
