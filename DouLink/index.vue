<template>
  <nuxt-link
    :to="localePath(to)"
    :exact="exact"
    class="relative hover:opacity-80 focus:outline-none focus:ring-2 focus:ring-offset-1"
    :class="`text-${color} font-${normal ? 'normal' : 'semibold'} focus:ring-${color}`"
    v-on="$listeners"
    v-bind="$attrs"
  >
    <!-- <div class="flex items-center"> -->
      <div v-if="warning" style="width: 0.5rem; height: 0.5rem" class="bg-orange-500 rounded-full animate-pulse ms-1 absolute -left-2"></div>
      {{ text }}
    <!-- </div> -->
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
    }
  }
}
</script>