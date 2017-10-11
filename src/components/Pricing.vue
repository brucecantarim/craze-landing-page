<template lang="pug">
  .pricing
    h2 {{ title }}
    p {{ text }}
    .list
      .box(v-for="plan in plans")
        .header
          h2 {{ plan.name }}
        .content
          ul
            h1 {{ plan.price.slice(0,3) }} #[small {{ plan.price.slice(4,6) }} ]
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
            feature1: 'Lorem Ipsum',
            feature2: 'Lorem Ipsum',
            feature3: 'Lorem Ipsum',
            feature4: 'Lorem Ipsum',
            feature5: 'Lorem Ipsum'
          }
        },
        standart: {
          name: 'Standart',
          price: '$39,99',
          features: {
            feature1: 'Lorem Ipsum',
            feature2: 'Lorem Ipsum',
            feature3: 'Lorem Ipsum',
            feature4: 'Lorem Ipsum',
            feature5: 'Lorem Ipsum'
          }
        },
        deluxe: {
          name: 'Deluxe',
          price: '$59,99',
          features: {
            feature1: 'Lorem Ipsum',
            feature2: 'Lorem Ipsum',
            feature3: 'Lorem Ipsum',
            feature4: 'Lorem Ipsum',
            feature5: 'Lorem Ipsum',
            feature6: 'Lorem Ipsum'
          }
        },
        unlimited: {
          name: 'Unlimited',
          price: '$79,99',
          features: {
            feature1: 'Lorem Ipsum',
            feature2: 'Lorem Ipsum',
            feature3: 'Lorem Ipsum',
            feature4: 'Lorem Ipsum',
            feature5: 'Lorem Ipsum'
          }
        }
      }
    }
  }
}
</script>

<style>
.pricing {
  background-color: gainsboro;
  box-sizing: border-box;
  padding: 10vh 20vw;
}
.list {
  display: flex;
  flex-direction: row;
  flex-flow: center;
}
.box {
  width: 100%;
  margin: 0 0.1rem;
  display: flex;
  flex-direction: column;
  flex-flow: center;
}
.header, .footer {
  background-color: #3498db;
}
.header h2 {
  color: white;
  padding: 0.5rem;
  margin: 0;
}
.footer {
  padding: 0.5rem;
  margin: 0;
}
.footer h4 {
  color: white;
  text-transform: uppercase;
}
a {
  text-decoration: none;
}
ul {
  background-color: white;
  list-style-position: outside;
  padding: 0;
  margin: 0;
}
li {
  width: 80%;
  margin: 0 auto;
  border-top: 1px solid #848484;
}
h1 {
  font-family: Novecentos, sans-serif;
  font-size: 2.5rem;
  margin: 0.2rem;
}
h1 small {
  font-size: 1.4rem;
  vertical-align: top;
}
</style>