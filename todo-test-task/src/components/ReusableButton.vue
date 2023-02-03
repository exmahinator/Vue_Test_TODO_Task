<template>
  <button :type="type" :class="className">
    {{ msg }}
  </button>
</template>

<script>
export default {
  name: "ReusableButton",
  props: {
    msg: String,
    className: String,
    type: {
      type: String,
      default: "button",
    },
  },
};
</script>
