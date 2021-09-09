<template>
  <label v-if="lable">{{ lable }}</label>
  <input
    class="field"
    :placeholder="lable"
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
    v-bind="$attr"
  />
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      default: ''
    },
    modelValue: {
      type: [String, Number],
      default: ''
    }
  }
}
</script>
