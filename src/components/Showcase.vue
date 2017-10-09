<template lang="pug">
    .showcase
        h2 {{ title }}
        p {{ text }}
        ul
            li(v-for="item in list")
                p {{ item }}
        video
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
      }
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
}
</style>