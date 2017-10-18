<template lang="pug">
  .features
    h2 {{ title }}
    p {{ placeholder }}
    ul
      li(v-for="feature in features")
        img(:src="feature.image") 
        h3 {{ feature.title }}
        p {{ placeholder.slice(0,59) + '.' }}
</template>

<script>
export default {
  name: 'Features',
  data () {
    return {
      title: 'Craze Features',
      features: {
        feat1: {
          title: 'Flat Design',
          image: require('../assets/icon-monitor.png')
        },
        feat2: {
          title: 'Marketable',
          image: require('../assets/icon-target.png')
        },
        feat3: {
          title: 'Edit Photos',
          image: require('../assets/icon-picture.png')
        },
        feat4: {
          title: 'Edit Colors',
          image: require('../assets/icon-pallet.png')
        },
        feat5: {
          title: 'User Friendly',
          image: require('../assets/icon-user.png')
        },
        feat6: {
          title: '100% Editable',
          image: require('../assets/icon-gear.png')
        }
      },
      placeholder: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
    }
  }
}
</script>

<style scoped>
.features {
  box-sizing: border-box;
  width: 100vw;
  padding: 10vh 20vw;
}

li {
  box-sizing: border-box;
  width: 15vw;
  padding: 2rem;
  display: inline-block;
  position: relative
} li:nth-child(2):after, li:nth-child(3):after, li:nth-child(5):after, li:nth-child(6):after {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  width: 80%;
  height: 80%;
  transform: translate(-63%, -50%);
  border-left: 1px solid gainsboro;
} li:nth-child(4):after, li:nth-child(5):before, li:nth-child(6):before {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  width: 80%;
  height: 80%;
  transform: translate(-50%, -63%);
  border-top: 1px solid gainsboro;
}
</style>