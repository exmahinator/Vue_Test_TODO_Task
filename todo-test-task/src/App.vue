<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <WelcomeTODO msg="This is my first message!"/>
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <!-- <reusableButton>This is my button</reusableButton>> -->
  <section class="section">
    <div class="container">
      <AddNotes/>
      <NotesList/>
    </div>
  </section>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import WelcomeTODO from "./components/WelcomeTODO.vue"
import AddNotes from "./components/AddNotes.vue"
import NotesList from "./components/NotesList.vue"

export default {
  name: 'App',
  components: {
    // HelloWorld,
    WelcomeTODO,
    AddNotes,
    NotesList
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
</style>
