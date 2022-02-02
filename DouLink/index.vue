<template>
  <nuxt-link
    :to="localePath(to)"
    :exact="exact"
    class="relative hover:opacity-80 focus:outline-none focus:ring-2 focus:ring-offset-1"
    :class="`text-${color} font-${normal ? 'normal' : 'semibold'} focus:ring-${color} bg-${bgColor}`"
    v-on="$listeners"
    v-bind="$attrs"
  >
    <div v-if="warning" style="width: 0.5rem; height: 0.5rem" class="bg-orange-500 rounded-full animate-pulse ms-1 absolute -left-2"></div>
    {{ text }}
  </nuxt-link>
</template>

<script>
export default {
  name: 'DouLink',
  props: {
    to: {
      type: String|Object,
      default: '/',
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
    },
    warning: {
      type: Boolean,
      default: false,
    },
    bgColor: {
      type: String,
      default: 'transparent',
    }
  }
}
</script>