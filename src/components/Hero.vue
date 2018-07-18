<template lang="pug">
  .hero
    .hero__content
      h1 {{ title }}
      h2 {{ slogan }}
      .hero__stores
        .hero__store-icon(v-for="store in stores")
          a(:href="store.link")
            img(:src="store.icon")
    .hero__mockup
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