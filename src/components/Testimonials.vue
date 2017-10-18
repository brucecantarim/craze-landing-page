<template lang="pug">
  carousel.testimonials(
    :autoplay="true" 
    :autoplayTimeout=4000
    :loop="true"
    :perPage=1
    :paginationPadding=0
    :paginationSize=12
    paginationColor="#FFFFFF"
    paginationActiveColor="#3498db"
    )
    slide.testimony(v-for="testimony in testimonials" :key="testimony.name")
      p {{ testimony.quote }}
      h5 {{ testimony.name }}
</template>

<script>
import { Carousel, Slide } from 'vue-carousel'

export default {
  name: 'Testimonials',
  components: {
    Carousel,
    Slide
  },
  data () {
    return {
      testimonials: {
        testimony1: {
          quote: 'Craze is one of the most complete app packages I have ever come across. I would highly reccomend it to anyone!',
          name: 'Sarah Hunt'
        },
        testimony2: {
          quote: 'Awesome. Period. Craze is the best. You should get it now!',
          name: 'John Smith'
        },
        testimony3: {
          quote: 'I don\'t know what I would do without Craze. Seriously.',
          name: 'Jane Smith'
        }
      }
    }
  }
}
</script>

<style>
.testimonials {
  padding: 5vh 0 8vh 0;
}.testimonials p {
  font-size: 1.2rem;
  font-style: italic;
}

.testimony {
  width: 100%;
}.testimony p:before { 
  content: open-quote; 
}.testimony p:after { 
  content: close-quote; 
}

.VueCarousel-dot-inner, .VueCarousel-dot-inner .VueCarousel-dot--active {
  margin: 0 0.2rem;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  border: 2px solid #3498db;
}.VueCarousel-dot-inner .VueCarousel-dot--active {
  background-color: #3498db;
}

/* ----------- Tablets ----------- */
@media screen 
  and (max-device-width: 768px)
  and (orientation: portrait) {
    
}

/* ----------- Smartphones ----------- */
@media screen 
  and (max-device-width: 600px),
  handheld and (orientation: landscape) {
    
}
</style>