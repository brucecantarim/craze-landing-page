<template lang="pug">
  .pricing
    .pricing__description
      h2 {{ title }}
      p {{ text }}
    .pricing__list
      .card(v-for="plan in plans")
        .card__header
          h2 {{ plan.name }}
        .card__content
          .card__price
            h1 {{ plan.price.slice(0,3) }} #[small {{ plan.price.slice(4,6) }} ]
          ul.card__list
            li.card__item(v-for="feature in plan.features") 
              p {{ feature }}
        .card__footer
          a(href="#")
            .card__button
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