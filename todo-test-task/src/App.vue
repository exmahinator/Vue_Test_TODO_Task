<template>
  <WelcomeTODO/>
  <section class="section">
    <div class="container">
      <AddNotes/>
      <NotesList/>
    </div>
  </section>
  <section class="section">
    <div class="container">
      <NewNote />
    </div>
  </section>
</template>

<script>
import WelcomeTODO from "./components/WelcomeTODO.vue"
import AddNotes from "./components/AddNotes.vue"
import NotesList from "./components/NotesList.vue"
import NewNote from "./components/NewNote.vue";

export default {
  name: 'App',
  components: {
    WelcomeTODO,
    AddNotes,
    NotesList,
    NewNote
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
}
</style>
