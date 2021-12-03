<template>
  <div>
    <DouLabel v-if="label" :label="label" />
    <input
      class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
      :class="{ 'border-red-300': error }"
      :id="id"
      :type="type"
      :placeholder="placeholder"
      v-bind="$attrs"
      v-on="inputListeners"
      :value="value"
    />
    <p v-if="hint" v-text="hint" class="text-gray-500 text-xs mt-2" />
    <p v-if="error" v-text="error" class="text-red-500 text-xs mt-2" />
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
    },
    hint: {
      type: String,
    },
    error: {
      type: String,
      default: '',
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