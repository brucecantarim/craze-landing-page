<template lang="pug">
  .hero
    img.iphone(src="../assets/iphone.png")
    h1 {{ title }}
    h2 {{ slogan }}
    .store-icons
      .icon-box(v-for="store in stores")
        a(:href="store.link")
          img(:src="store.icon")
</template>

<script>
export default {
  name: 'Hero',
  data () {
    return {
      title: 'Craze',
      slogan: 'A great new psd theme to showcase your new app.',
      stores: {
        apple: {
          name: 'Apple Store',
          icon: require('../assets/apple.svg'),
          link: 'http://itunes.apple.com'
        },
        android: {
          name: 'Google Play Store',
          icon: require('../assets/android.svg'),
          link: 'http://play.google.com'
        },
        windows: {
          name: 'Windows Store',
          icon: require('../assets/windows.svg'),
          link: 'http://store.windows.com'
        }
      }
    }
  }
}
</script>

<style scoped>
.hero {
  box-sizing: border-box;
  background-color: blue;
  background-image: url('../assets/pattern.png');
  height: 60vh;
  width: 100vw;
  padding: 10vh 20vw;
  text-align: left;
  overflow: hidden;
  position: relative;
}

h1 {
  font-family: Pacifico, cursive;
  font-weight: bold;
  font-size: 4rem;
}

h2 {
  font-weight: normal;
  max-width: 45%;
}

h1,
h2 {
  color: white;
  text-shadow: 0 0.3rem 0 rgba(0, 0, 0, 0.2);
}

a {
  color: #42b983;
}

.iphone {
  float: right;
  position: absolute;
  bottom: 0;
  right: 20vw;
}

.icon-box {
  display: inline-block;
  padding: 5px;
  margin-right: 0.5rem;
  width: 40px;
  height: 40px;
  background-color: black;
  border-radius: 50%;
  filter: grayscale(1) opacity(0.5);
}.icon-box:hover {
  filter: grayscale(0) opacity(1);
}.icon-box img {
  margin-top: 20%;
  width: 100%;
  height: 60%;
}
</style>
