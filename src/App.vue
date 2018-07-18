<template lang="pug">
  #app
    hero
    features
    showcase
    testimonials
    pricing
    social
    links
</template>

<script>
import Hero from './components/Hero'
import Features from './components/Features'
import Showcase from './components/Showcase'
import Testimonials from './components/Testimonials'
import Pricing from './components/Pricing'
import Social from './components/Social'
import Links from './components/Links'

export default {
  name: 'app',
  components: {
    Hero,
    Features,
    Showcase,
    Testimonials,
    Pricing,
    Social,
    Links
  }
}
</script>

<style lang="scss">
// Here we import the main Sass file, with the styles that will be applied all over the app
@import './sass/style.scss';
</style>
