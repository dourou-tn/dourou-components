<template>
  <Nuxt-link :to="localePath('/')">
    <img
      :class="`w-${width} ${ light ? 'block' : 'hidden sm:block' }`"
      :src="logo_light"
    />
    <img
      v-if="!light"
      :class="`w-${width}`"
      :src="logo_dark"
      class="block sm:hidden"
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
      }
    },
    data () {
      return {
        logo_light: require('~/assets/image/logo-light.png'),
        logo_dark: require('~/assets/image/logo-dark.png'),
        lightClass: ''
      }
    }
  }
</script>
