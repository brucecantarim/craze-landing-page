<template lang="pug">
.links
  ul
    li(v-for="link in links")
      a(:href="link.url") {{ link.name }}
</template>

<script>
export default {
  name: 'Social',
  data () {
    return {
      links: {
        contact: {
          name: 'Contact',
          url: 'mailto:contact@craze.com'
        },
        download: {
          name: 'Download',
          url: 'http://freebiesxpress.com/gallery/craze-free-psd-template/'
        },
        press: {
          name: 'Press',
          url: 'http://blazrobar.com/free-psd-website-templates/craze-trendy-landing-page-website-design/'
        },
        mail: {
          name: 'Mail',
          url: 'mailto:craze@craze.com'
        },
        support: {
          name: 'Support',
          url: 'https://themeforest.net/item/craze-app-landing-psd-template/19354545/comments'
        },
        policy: {
          name: 'Privacy Policy',
          url: 'https://www.google.com/policies/privacy/'
        }
      }
    }
  }
}
</script>

<style scoped>
.links {
  background-color: gainsboro;
  padding: 3vh 20vw;
}
li {
  display: inline;
  margin: 1rem;
}
a {
  font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
  font-size: 0.8rem;
  color: gray;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
</style>

