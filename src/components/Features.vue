<template lang="pug">
    .features
        h2 {{ title }}
        p {{ placeholder }}
        ul
            li(v-for="feature in features") 
                h3 {{ feature }}
                p {{ placeholder }}
</template>

<script>
export default {
  name: 'Features',
  data () {
    return {
      title: 'Craze Features',
      features: {
        feat1: 'Flat Design',
        feat2: 'Marketable',
        feat3: 'Edit Photos',
        feat4: 'Edit Colors',
        feat5: 'User Friendly',
        feat6: '100% Editable'
      },
      placeholder: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
    }
  }
}
</script>

<style scoped>
.features{
    box-sizing: border-box;
    width: 100vw;
    padding: 10vh 20vw;
}

li {
    box-sizing: border-box;
    width: 15vw;
    padding: 2rem;
    display: inline-block;
}
</style>