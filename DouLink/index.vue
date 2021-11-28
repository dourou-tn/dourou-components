<template>
  <Nuxt-link :to="to" class="text-purple tracking-wider">
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
    }
  }
}
</script>