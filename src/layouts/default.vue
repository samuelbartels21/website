<template>
  <div>
    <navbar :links="navbarLinks"></navbar>
    <banner class="p__banner">COVID UPDATE</banner>
    <nuxt class="p__content"></nuxt>
    <footer-section :links="footerLinks"></footer-section>
    <cookies />
  </div>
</template>

<script>
  import Banner from '~/components/Banner'
  import FooterSection from '~/components/Footer'
  import Navbar from '~/components/Navbar'

  export default {
    components: {
      Banner,
      Cookies: () => import('~/components/Cookies'),
      Navbar,
      FooterSection,
    },

    created() {
      this.navbarLinks = [
        {
          href: 'https://www.meetup.com/vuejs-london/',
          rel: 'noopener',
          target: '_blank',
          text: 'Meetup',
        },
        { to: '/2019', text: '2019' },
        { to: '/2018', text: '2018' },
      ]

      this.footerLinks = [
        {
          href:
            'https://london.us16.list-manage.com/subscribe?u=1c418a486ef9ef69a14c73464&id=6450120068',
          target: '_blank',
          rel: 'noopener',
          text: 'Newsletter',
        },
        {
          href:
            'https://join.slack.com/t/vuejsconferences/shared_invite/enQtMzY5Njg2NjA2NTAxLTU4NTA5YTViMGJiYmNhZTRmYTE2YzEwNDdhYjA2ZDJiYjE4OTZlYjcwYzFkZDkyNGNmYTU2NDczNGVhYzFiOWU',
          target: '_blank',
          rel: 'noopener',
          text: 'Slack',
        },
        {
          href: 'https://www.meetup.com/vuejs-london/',
          rel: 'noopener',
          target: '_blank',
          text: 'Meetup',
        },
        {
          href: 'https://shop.spreadshirt.co.uk/vue-london/',
          rel: 'noopener',
          target: '_blank',
          text: 'Store',
        },
        { to: '/2019', text: '2019' },
        { to: '/2018', text: '2018' },

        { to: '/code-of-conduct', text: 'Code of Conduct' },
        { to: '/terms-and-conditions', text: 'Terms and Conditions' },
        { to: '/privacy-policy', text: 'Privacy Policy' },
      ]
    },

    head: {
      meta: [
        { charset: 'utf-8' },
        { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      ],
    },
  }
</script>

<style lang="postcss" scoped>
  .p__banner {
    position: fixed;
    z-index: var(--z-index-navbar);
  }

  .p__content {
    padding-top: var(--grid-ten);
  }
</style>
