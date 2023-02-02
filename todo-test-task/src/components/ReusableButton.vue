<template>
// import Vue from "vue";

// const Button = Vue.component("reusableButton", {
//   render(createElement, props) {
//     return createElement("button", props, this.$slots.default);
//   },
// });

// export default Button;
<div class="welcome">
    <h1>Simple TODO</h1>
    <p>{{ msg }}</p>
    <button type="button">Click me!</button>
</div>
</template>

<script>
export default {
    name: 'WelcomeTODO',
    props: {
        msg: String
    }
}
</script>
