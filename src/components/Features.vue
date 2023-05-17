<template lang="pug">
  .features
    .features__description
      h2 {{ title }}
      p {{ (description != '') ? description : placeholder }}
    ul.features__list
      li.features__item(v-for="feature in features")
        img(:src="feature.image") 
        h3 {{ feature.title }}
        p {{ (feature.description != '') ? feature.description : placeholder.slice(0,55) + '.' }}
</template>

<script>
export default {
  name: 'Features',
  data () {
    return {
      title: 'Craze Features',
      description: '',
      features: {
        feat1: {
          title: 'Flat Design',
          description: '',
          image: require('../assets/icon-monitor.png')
        },
        feat2: {
          title: 'Marketable',
          description: '',
          image: require('../assets/icon-target.png')
        },
        feat3: {
          title: 'Edit Photos',
          description: '',
          image: require('../assets/icon-picture.png')
        },
        feat4: {
          title: 'Edit Colors',
          description: '',
          image: require('../assets/icon-pallet.png')
        },
        feat5: {
          title: 'User Friendly',
          description: '',
          image: require('../assets/icon-user.png')
        },
        feat6: {
          title: '100% Editable',
          description: '',
          image: require('../assets/icon-gear.png')
        }
      },
      placeholder: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
    }
  }
}
</script>