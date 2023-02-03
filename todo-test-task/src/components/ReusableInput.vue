<template>
  <label :class="labelClass"
    ><span :class="spanClass">{{ label }}</span
    ><input
      :placeholder="inputPlaceholder"
      :class="inputClass"
      :type="inputType"
      :disabled="isDisabled"
      :checked="isChecked"
  /></label>
</template>

<script>
export default {
  name: "ReusableInput",
  props: {
    label: {
      type: String,
      default: "",
    },
    inputPlaceholder: {
      type: String,
      default: "",
    },
    inputType: {
      type: String,
      default: "text",
    },
    isDisabled: {
      type: Boolean,
      default: true,
    },
    isChecked: {
      type: Boolean,
      default: false,
    },
    labelClass: String,
    inputClass: String,
    spanClass: String,
  },
};
</script>
