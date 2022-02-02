<template>
  <div class="grid gap-4 lg:gap-3 sm:gap-5 grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-2 xl:grid-cols-3 ">
    <slot />
  </div>
</template>
<script>
export default {
  name: 'DouGrid',
}
</script>
