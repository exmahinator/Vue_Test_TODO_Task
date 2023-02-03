<template>
  <ul class="notesList">
    <li class="notesItem">
      <div class="notesSubCointainer notesButtons">
        <!-- <button type="button" class="notesEdit">Edit the scroll!</button>
                <button type="button" class="notesDelete">Burn it down!</button> -->
        <!-- <button type="button" class="notesBtn notesEdit">Edit</button>
                <button type="button" class="notesBtn notesDelete">Delete</button> -->
        <ReusableButton className="notesBtn notesEdit" msg="Edit the scroll" />
        <ReusableButton className="notesBtn notesDelete" msg="Burn it down!" />
      </div>
      <div class="notesSubCointainer notesTask">
        <h2>Task one</h2>
        <ol>
          <li class="notesSubItem">
            <!-- <label class="notesLabel">My subtask #1<input type="checkbox" class="notesInput" disabled checked></label> -->
            <ReusableInput
              labelClass="notesLabel"
              inputClass="notesInput"
              label="My subtask #1"
              inputType="checkbox"
              isDisabled
              isChecked
            />
          </li>
          <li class="notesSubItem">
            <label class="notesLabel"
              >My subtask #2<input type="checkbox" class="notesInput" disabled
            /></label>
          </li>
          <li class="notesSubItem">
            <label class="notesLabel"
              >My subtask #3<input type="checkbox" class="notesInput" disabled
            /></label>
          </li>
          <li class="notesSubItem">
            <label class="notesLabel"
              >My subtask #4<input type="checkbox" class="notesInput" disabled
            /></label>
          </li>
          <!-- <li v-for="(task, index) in myList" :key="index"><ReusableInput labelClass="notesLabel" inputClass="notesInput" :label=task.todo inputType="checkbox" isDisabled :isChecked=task.isDone /></li> -->
        </ol>
      </div>
    </li>
    <li class="notesItem">
      <div class="notesSubCointainer notesButtons">
        <ReusableButton className="notesBtn notesEdit" msg="Edit the scroll" />
        <ReusableButton className="notesBtn notesDelete" msg="Burn it down!" />
      </div>
      <div class="notesSubCointainer notesTask">
        <h2>Task two</h2>
        <ol>
          <li class="notesSubItem">
            <label class="notesLabel"
              >My subtask #1<input type="checkbox" class="notesInput" disabled
            /></label>
          </li>
          <li class="notesSubItem">
            <label class="notesLabel"
              >My subtask #2<input type="checkbox" class="notesInput" disabled
            /></label>
          </li>
        </ol>
      </div>
    </li>
    <li class="notesItem">
      <div class="notesSubCointainer notesButtons">
        <ReusableButton className="notesBtn notesEdit" msg="Edit the scroll" />
        <ReusableButton className="notesBtn notesDelete" msg="Burn it down!" />
      </div>
      <div class="notesSubCointainer notesTask">
        <h2>Task three</h2>
        <ol>
          <li
            class="notesSubItem"
            v-for="(task, index) in myListTwo"
            :key="index"
          >
            <ReusableInput
              labelClass="notesLabel"
              inputClass="notesInput"
              spanClass="notesText"
              :label="task.todo"
              inputType="checkbox"
              isDisabled
              :isChecked="task.isDone"
            />
          </li>
        </ol>
      </div>
    </li>
    <!-- <li class="notesItem">
            <div class="notesSubCointainer notesButtons">
                <ReusableButton className="notesBtn notesEdit" msg="Edit the scroll" />
                <ReusableButton className="notesBtn notesDelete" msg="Burn it down!" />
            </div>
            <div class="notesSubCointainer notesTask">
                <h2>Task four</h2>
                <ol>
                    <li class="notesSubItem" v-for="(task, index) in myListTwo" :key="index"><ReusableInput labelClass="notesLabel" inputClass="notesInput" spanClass="notesText" :label=task.todo inputType="checkbox" isDisabled :isChecked=task.isDone /></li>
                </ol>
            </div>
        </li> -->
    <li class="notesItem" v-for="myTask in myList" :key="myTask.noteId">
      <div class="notesSubCointainer notesButtons">
        <ReusableButton className="notesBtn notesEdit" msg="Edit the scroll" />
        <ReusableButton className="notesBtn notesDelete" msg="Burn it down!" />
      </div>
      <div class="notesSubCointainer notesTask">
        <h2>{{ myTask.noteTitle }}</h2>
        <ol>
          <li
            class="notesSubItem"
            v-for="task in myTask.todoList"
            :key="task.id"
          >
            <ReusableInput
              labelClass="notesLabel"
              inputClass="notesInput"
              spanClass="notesText"
              :label="task.todo"
              inputType="checkbox"
              isDisabled
              :isChecked="task.isDone"
            />
          </li>
        </ol>
      </div>
    </li>
  </ul>
</template>

<script>
import ReusableButton from "./ReusableButton.vue";
import ReusableInput from "./ReusableInput.vue";
export default {
  name: "NotesList",
  components: {
    ReusableButton,
    ReusableInput,
  },
  data() {
    return {
      // myList: ["At first I would like to install Windows", "At second I need to install proper drivers", "After that I need to install basic programs", "Finally I can install any other programs or games - depends what I want to be installed"]
      myListTwo: [
        {
          todo: "At first I would like to install Windows",
          id: "1a",
          isDone: true,
        },
        {
          todo: "At second I need to install proper drivers",
          id: "2a",
          isDone: true,
        },
        {
          todo: "After that I need to install basic programs",
          id: "3a",
          isDone: false,
        },
        {
          todo: "Finally I can install any other programs or games - depends what I want to be installed",
          id: "4a",
          isDone: false,
        },
      ],
      myList: [
        {
          noteId: "n1",
          noteTitle: "My Task Four",
          todoList: [
            {
              todo: "At first I would like to install Windows",
              id: "1a",
              isDone: true,
            },
            {
              todo: "At second I need to install proper drivers",
              id: "2a",
              isDone: true,
            },
            {
              todo: "After that I need to install basic programs",
              id: "3a",
              isDone: false,
            },
          ],
        },
        {
          noteId: "n2",
          noteTitle: "My Task Five",
          todoList: [
            {
              todo: "At first I would like to install Windows",
              id: "1a",
              isDone: true,
            },
            {
              todo: "At second I need to install proper drivers",
              id: "2a",
              isDone: true,
            },
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
@import "../styles/notesStyles.css";
</style>
