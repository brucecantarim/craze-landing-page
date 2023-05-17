<template lang="pug">
  .showcase
    .showcase__about
      h2 {{ title }}
      p {{ text }}
      ul.showcase__list
        li.showcase__item(v-for="item in list")
          p {{ item }}
    video.showcase__video(controls :poster="poster")
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