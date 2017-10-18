<template lang="pug">
  .pricing
    h2 {{ title }}
    p {{ text }}
    .pricing-list
      .box(v-for="plan in plans")
        .header
          h2 {{ plan.name }}
        .content
          .price
            h1 {{ plan.price.slice(0,3) }} #[small {{ plan.price.slice(4,6) }} ]
          ul
            li(v-for="feature in plan.features") 
              p {{ feature }}
        .footer
          a(href="#")
            .button
              h4 {{ action }}
</template>

<script>
export default {
  name: 'Pricing',
  data () {
    return {
      title: 'Pricing Plans',
      text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
      action: 'Purchase',
      plans: {
        basic: {
          name: 'Basic',
          price: '$19,99',
          features: {
            feature1: 'Feature 1',
            feature2: 'Feature 2',
            feature3: 'Feature 3',
            feature4: 'Feature 4',
            feature5: 'Feature 5'
          }
        },
        standart: {
          name: 'Standart',
          price: '$39,99',
          features: {
            feature1: 'Feature 1',
            feature2: 'Feature 2',
            feature3: 'Feature 3',
            feature4: 'Feature 4',
            feature5: 'Feature 5'
          }
        },
        deluxe: {
          name: 'Deluxe',
          price: '$59,99',
          features: {
            feature1: 'Feature 1',
            feature2: 'Feature 2',
            feature3: 'Feature 3',
            feature4: 'Feature 4',
            feature5: 'Feature 5',
            feature6: 'Feature 6'
          }
        },
        unlimited: {
          name: 'Unlimited',
          price: '$79,99',
          features: {
            feature1: 'Feature 1',
            feature2: 'Feature 2',
            feature3: 'Feature 3',
            feature4: 'Feature 4',
            feature5: 'Feature 5'
          }
        }
      }
    }
  }
}
</script>

<style scoped>
.pricing {
  background-color: gainsboro;
  box-sizing: border-box;
  padding: 10vh 20vw;
  height: 70vh;
}

.pricing-list {
  box-sizing: border-box;
  padding: 0 -20vw;
  display: flex;
  flex-direction: row;
  justify-content: center;
  flex-flow: center;
}

.box {
  width: 100%;
  margin: 25px 0.1rem;
  display: flex;
  flex-direction: column;
  flex-flow: center;
}.box:nth-child(3n) {
  margin: 0 0.1rem 25px 0.1rem;
}

.header, .footer {
  background-color: #3498db;
}.header h2 {
  color: white;
  padding: 0.5rem;
  margin: 0;
}

.content {
  background-color: white;
}

.footer {
  padding: 0.5rem;
  margin: 0;
}.footer h4 {
  color: white;
  text-transform: uppercase;
}

a {
  text-decoration: none;
}

ul {
  list-style-position: outside;
  padding: 0;
  margin: 0;
  height: 100%;
} 

li {
  width: 80%;
  margin: 0 auto;
  border-top: 1px solid #848484;
}

.price {
  height: 4rem;
  padding: 0.5rem 0;
}

h1 {
  font-family: Novecentos, sans-serif;
  font-size: 2.5rem;
  margin: 0;
} h1 small {
  font-size: 1.4rem;
  vertical-align: 35%;
  margin: -0.5rem;
}

.button {
  cursor: pointer;
  background-color: #0d74b9;
  max-width: 65%;
  min-height: 2.5rem;
  margin: 0.5rem auto;
  display: flex;
  flex-direction: column;
  flex-flow: center;
  justify-content: center;
} a .button:hover{
  background-color: rgba(100,200,255,1);
}

h4 {
  margin: 0 auto;
  line-height: 0;
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
    
}
</style>