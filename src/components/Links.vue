<template lang="pug">
.links
  ul.links__list
    li.links__item(v-for="link in links")
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
          url: 'mailto:bruce@cantarim.com'
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
          url: 'mailto:bruce@cantarim.com'
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