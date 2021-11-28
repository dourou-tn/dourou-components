<template>
  <div>
    <DouLabel v-if="label" :label="label" />
    <input
      class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
      :id="id"
      :type="type"
      :placeholder="placeholder"
      v-bind="$attrs"
      v-on="inputListeners"
      :value="value"
    />
  </div>
</template>

<script>
import DouLabel from '../DouLabel/index.vue';

export default {
  name: 'DouInput',
  components: { DouLabel },
  props: {
    value: {},
    type: {
      type: String,
      default: 'text',
    },
    id: {
      type: String,
    },
    placeholder: {
      type: String,
    },
    label: {
      type: String,
    }
  },
  computed: {
    inputListeners: function () {
      let vm = this;
      return Object.assign(
         {},
         this.$listeners,
         {
           input: function(e) {
             vm.$emit('input', e.target.value);
           }
         }
      )
    }
  }
}
</script>