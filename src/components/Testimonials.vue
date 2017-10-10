<template lang="pug">
  .testimonials
    .testimony(v-for="testimony in testimonials")
      p {{ testimony.quote }}
      h5 {{ testimony.name }}
    .dots
      .dot-active
      .dot
      .dot
</template>

<script>
export default {
  name: 'Testimonials',
  data () {
    return {
      testimonials: {
        testimony1: {
          quote: 'Craze is one of the most complete app packages I have ever come across. I would highly reccomend it to anyone!',
          name: 'Sarah Hunt'
        },
        testimony2: {
          quote: 'Craze is one of the most complete app packages I have ever come across. I would highly reccomend it to anyone!',
          name: 'Sarah Hunt'
        },
        testimony3: {
          quote: 'Craze is one of the most complete app packages I have ever come across. I would highly reccomend it to anyone!',
          name: 'Sarah Hunt'
        }
      }
    }
  }
}
</script>

<style scoped>
.testimonials {
  padding: 5vh 24vw;
}
p {
  font-size: 1.2rem;
  font-style: italic;
}

p:before { 
  content: open-quote; 
}

p:after { 
  content: close-quote; 
}

.testimony {
  display: none;
}

.testimony:first-of-type {
  display: block;
}

.dots {
  margin: 1rem auto;
}

.dot, .dot-active {
  display: inline-block;
  margin: 0 0.2rem;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  border: 2px solid #3498db;
}

.dot-active {
  background-color: #3498db;
}

</style>