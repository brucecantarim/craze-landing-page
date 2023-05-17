<template lang="pug">
  div.testimonials
    div.testimonials__item
      p {{ currentSlide.quote }}
      h5 {{ currentSlide.name }}
    div.testimonials__counter
      div.testimonials__dot(
        v-for="(testimony, index) in testimonials"
        :key="testimony.id"
        :class="[(activeSlide == index) ? 'testimonials__dot--active' : '']"
        @click="goToSlide(index);"
      )
</template>

<script>
export default {
  name: 'Testimonials',
  data () {
    return {
      testimonials: [
        {
          id: 1,
          quote: 'Craze is one of the most complete app packages I have ever come across. I would highly reccomend it to anyone!',
          name: 'Sarah Hunt'
        },
        {
          id: 2,
          quote: 'Awesome. Period. Craze is the best. You should get it now!',
          name: 'John Smith'
        },
        {
          id: 3,
          quote: 'I don\'t know what I would do without Craze. Seriously.',
          name: 'Jane Doe'
        }
      ],
      activeSlide: 0,
      auto: true
    }
  },
  mounted () {
    // When the testimonials component is mounted, we start the slider
    if (this.auto === true) {
      this.autoInterval = setInterval(() => {
        this.next()
      }, 4000)
    }
  },
  computed: {
    // Here we define the function to get the current active slide
    currentSlide () {
      return this.testimonials[this.activeSlide]
    }
  },
  methods: {
    // Here we implement the function to get the next slide of the carousel
    next () {
      let active = this.activeSlide + 1
      if (active >= this.testimonials.length) {
        active = 0
      }
      this.activateSlide(active)
    },
    // Here we define the function to activate a slide via argument
    activateSlide (slideIndex) {
      this.activeSlide = slideIndex
    },
    // Here we implement the function that disables the autoslider timer
    disableAutoInterval () {
      this.auto = false
      clearInterval(this.autoInterval)
    },
    // And here we call both disableAutoInterval() and activateSlide() when the user interacts with the controls
    goToSlide (slideIndex) {
      this.disableAutoInterval()
      this.activateSlide(slideIndex)
    }
  }
}
</script>