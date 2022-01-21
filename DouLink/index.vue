<template>
  <nuxt-link
    :to="localePath(to)"
    :exact="exact"
    class="focus:outline-none focus:ring-2 focus:ring-offset-1 "
    :class="`text-${color} font-${normal ? 'normal' : 'semibold'} focus:ring-${color}`"
    v-on="$listeners"
    v-bind="$attrs"
  >
    {{ text }}
  </nuxt-link>
</template>

<script>
export default {
  name: 'DouLink',
  props: {
    to: {
      type: String|Object,
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
    },
    styles: {
      type: String,
      default: '',
    },
    normal: {
      type: Boolean,
      default: false,
    }
  }
}
</script>