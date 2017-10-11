<template lang="pug">
  .showcase
    .about
      h2 {{ title }}
      p {{ text }}
      ul
        li(v-for="item in list")
          p {{ item }}
    video(controls :poster="poster")
      source(src="#" type="video/webm")
</template>

<script>
export default {
  name: 'Showcase',
  data () {
    return {
      title: 'Whats Craze all about?',
      text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
      list: {
        item1: 'Lorem ipsum',
        item2: 'Lorem ipsum'
      },
      poster: require('../assets/video.png')
    }
  }
}
</script>

<style scoped>
.showcase {
  background-color: gainsboro;
  box-sizing: border-box;
  padding: 10vh 20vw;
  text-align: left;
  display: flex;
  flex-direction: row;
  flex-flow: center;
}

.about {
  width: 100%;
  display: inline-block;
  padding-right: 5rem;
}

li {
  list-style: outside url('../assets/bullet.png');
}

video {
  width: 70%;
  height: auto;
  display: inline-block;
  background-color: black;
  border-radius: 10px;
  margin-top: 1rem;
}
</style>