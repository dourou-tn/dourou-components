<template>
  <!-- custom select component  -->
  <select
    v-model="value"
    v-on="$listeners"
    @change="change"
    class="select select-bordered select-primary w-full"
  >
    <option
      v-for="item in items"
      :value="item.value"
      :key="item.id"
    >
      {{ item.label }}
    </option> 
  </select>
</template>

<script>
export default {
  name: 'DouSelect',
  props: {
    value: {},
    items: {
      type: Array,
      required: true
    }
  },
  methods: {
    change(e) {
      this.$emit('change', e.target.value)
    }
  },
}
</script>