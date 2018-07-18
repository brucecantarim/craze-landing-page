<template lang="pug">
.social
  .social__description
    h2 {{ title }}
    p {{ text }}
  .social__list
    .social__icon(v-for="network in networks")
      a(:href="network.link")
        img(:src="network.icon")
</template>

<script>
export default {
  name: 'Social',
  data () {
    return {
      title: 'Say Hi & Get in Touch',
      text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod.',
      networks: {
        twitter: {
          name: 'Twitter',
          icon: require('../assets/twitter.svg'),
          link: 'http://www.twitter.com'
        },
        facebook: {
          name: 'Facebook',
          icon: require('../assets/facebook.svg'),
          link: 'http://www.facebook.com'
        },
        pinterest: {
          name: 'Pinterest',
          icon: require('../assets/pinterest.svg'),
          link: 'http://www.pinterest.com'
        },
        gplus: {
          name: 'Google+',
          icon: require('../assets/google-plus.svg'),
          link: 'http://plus.google.com'
        },
        linkedin: {
          name: 'Twitter',
          icon: require('../assets/linkedin.svg'),
          link: 'http://www.linkedin.com'
        },
        youtube: {
          name: 'Youtube',
          icon: require('../assets/youtube.svg'),
          link: 'http://www.youtube.com'
        }
      }
    }
  }
}
</script>