<template>
  <div>
    <img :src="imgPath" alt="" :class="imgClass">
  </div>
</template>

<script>
  export default {
    name: 'DouBanner',
    props: {
      imgClass: {
        type: String,
        default: 'mx-auto'
      },
      'img-path': {
        type: String,
        required: true,
      }
    }
  }
</script>