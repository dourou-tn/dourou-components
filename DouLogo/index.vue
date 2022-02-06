<template>
  <Nuxt-link :to="localePath('/')" class="cursor-pointer">
    <nuxt-img
      :class="`${ light ? 'block' : 'hidden sm:block' }`"
      :src="logo_light"
    />
    <nuxt-img
      v-if="!light && dark"
      :src="logo_dark"
      :class="`${ dark ? 'block' : 'hidden sm:block' }`"
    />
  </Nuxt-link>
</template>
<script>
  export default {
    name: 'DouLogo',
    props: {
      width: {
        default: 24,
      },
      // If passed true only the light version of the logo will be shown
      light: {
        type: Boolean,
        default: false
      },
      dark: {
        type: Boolean,
        default: false
      }
    },
    data () {
      return {
        logo_light: '/logo-light-new-sm.png',
        logo_dark: '/logo-dark-new-sm.png',
        lightClass: ''
      }
    }
  }
</script>
