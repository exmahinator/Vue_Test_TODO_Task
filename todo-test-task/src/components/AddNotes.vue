<template>
  <!-- <div class="addNoteContainer"><button type="button" class="addNoteBtn">{{ msg }}</button></div> -->
  <div class="addNoteContainer">
    <ReusableButton className="addNoteBtn" msg="Add a new note!" />
  </div>
  <!-- <div class="addNoteContainer"><slot></slot></div> -->
</template>

<script>
import ReusableButton from "./ReusableButton.vue";
export default {
  name: "AddNotes",
  // props: {
  //     msg: String
  // },
  components: {
    ReusableButton,
  },
};
</script>

<style scoped>
@import "../styles/addNewNoteBtn.css";
</style>
