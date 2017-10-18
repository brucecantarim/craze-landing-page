<template lang="pug">
.social
  h2 {{ title }}
  p {{ text }}
  .social-icons
    .icon-box(v-for="network in networks")
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

<style scoped>
.social{
  padding-top: 10vh;
  padding-bottom: 5vh;
}

.icon-box {
  display: inline-block;
  padding: 1px;
  margin: 0.5rem;
  width: 30px;
  height: 30px;
  filter: grayscale(1) opacity(0.5);
}.icon-box:hover {
  filter: grayscale(0) opacity(1);
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
    .social {
      padding: 5vh 5vw;
    }
    .icon-box {
      width: 100px;
      height: 100px;
    }
}
</style>