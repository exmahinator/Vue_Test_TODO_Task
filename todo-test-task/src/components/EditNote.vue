<template>
  <ul class="notesList">
    <li class="notesItem">
      <div class="notesSubCointainer notesTask">
        <h2>Task one</h2>
        <ol>
          <li class="notesSubItem">
            <label class="notesLabel"
              >My subtask #1<input type="checkbox" class="notesInput"
            /></label>
          </li>
          <li class="notesSubItem">
            <label class="notesLabel"
              >My subtask #2<input type="checkbox" class="notesInput"
            /></label>
          </li>
          <li class="notesSubItem">
            <label class="notesLabel"
              >My subtask #3<input type="checkbox" class="notesInput"
            /></label>
          </li>
          <li class="notesSubItem">
            <label class="notesLabel"
              >My subtask #4<input type="checkbox" class="notesInput"
            /></label>
          </li>
        </ol>
      </div>
    </li>
  </ul>
</template>

<script>
export default {
  name: "EditNote",
};
</script>

<style scoped>
@import "../styles/notesStyles.css";
</style>
