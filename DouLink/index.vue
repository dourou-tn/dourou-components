<template>
  <Nuxt-link :to="localePath(to)" :class="`text-${color}`" class="font-semibold tracking-wider" :exact="exact">
    {{ text }}
  </Nuxt-link>
</template>

<script>
export default {
  name: 'DouLink',
  props: {
    to: {
      type: String,
      required: true
    },
    text: {
      type: String,
      required: true
    },
    color: {
      type: String,
      default: 'purple-500'
    },
    exact: {
      type: Boolean,
      default: false,
    }
  }
}
</script>