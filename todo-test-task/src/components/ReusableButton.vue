<template>
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
