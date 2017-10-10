<template lang="pug">
  .hero
    img(src="../assets/iphone.png")
    h1 {{ title }}
    h2 {{ slogan }}
</template>

<script>
export default {
  name: 'Hero',
  data () {
    return {
      title: 'Craze',
      slogan: 'A great new psd theme to showcase your new app.'
    }
  }
}
</script>

<style scoped>
div {
  box-sizing: border-box;
  background-color: blue;
  background-image: url('../assets/pattern.png');
  height: 60vh;
  width: 100vw;
  padding: 10vh 20vw;
  text-align: left;
  overflow: hidden;
}

h1 {
  font-family: Pacifico, cursive;
  font-weight: bold;
  font-size: 4rem;
}

h2 {
  font-weight: normal;
}

h1,
h2 {
  color: white;
  text-shadow: 0 0.3rem 0 rgba(0, 0, 0, 0.2);
}

a {
  color: #42b983;
}

img {
  float: right;
}
</style>
