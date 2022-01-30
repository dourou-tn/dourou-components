<template>
  <!-- <img :src="imgPath" alt="" :class="imgClass"> -->
  <nuxt-img :src="imgPath" alt="" :class="imgClass"></nuxt-img>
</template>

<script>
  export default {
    name: 'DouBanner',
    props: {
      imgClass: {
        type: String,
        default: 'shadow-md'
      },
      'img-path': {
        type: String,
        required: true,
      }
    }
  }
</script>