<template>
<svg :fill="color" :width="width" :height="height" version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 16 16" style="enable-background:new 0 0 16 16;" xml:space="preserve">
  <g>
    <g>
      <path d="M8,0C3.589,0,0,3.589,0,8s3.589,8,8,8s8-3.589,8-8S12.411,0,8,0z M8,14c-3.309,0-6-2.691-6-6s2.691-6,6-6s6,2.691,6,6
			S11.309,14,8,14z" />
      <polygon points="9,4 7,4 7,7 4,7 4,9 7,9 7,12 9,12 9,9 12,9 12,7 9,7 		" />
    </g>
  </g>
</svg>
</template>
<script>
export default {
  name: 'IconAdd',
  props: {
    width: {
      type: Number,
      default: 24,
    },
    height: {
      type: Number,
      default: 24,
    },
    color: {
      type: String,
      default: 'purple',
    },
  },
}
</script>
