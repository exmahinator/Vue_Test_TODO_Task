<template>
  <form class="newNoteContainer">
    <div class="newNoteSubContainer topRound">
      <h2 class="newNoteHeader">Adding the note...</h2>
    </div>
    <div class="newNoteSubContainer">
      <!-- <label class="newNoteLabel"><span class="newNoteText">What needs to be planned:</span><input type="text" name="noteTitle" class="newNoteInput flexGrow"
                            placeholder="Hey, here you must enter the title of new note..."></label> -->
      <ReusableInput
        labelClass="newNoteLabel"
        inputClass="newNoteInput flexGrow"
        spanClass="newNoteText"
        inputType="text"
        label="What needs to be planned:"
        inputPlaceholder="Hey, here you must enter the title of new note..."
        :isDisabled="false"
      />
      <div class="newNoteAddTodoContainer">
        <label class="newNoteLabel flexGrow"
          ><span class="newNoteText">Add todo:</span
          ><input
            type="text"
            name="noteTodo"
            class="newNoteInput flexGrow"
            placeholder="Add some todos to your note"
        /></label>
        <button type="button" class="newNoteBtn">Add me!</button>
      </div>
    </div>
    <div class="newNoteSubContainer bottomRound">
      <div class="newNoteResultContainer">
        <h2 class="newNoteResultHeader">
          <span class="newNoteResultText">Result title:</span>Task one
        </h2>
        <div class="newNotesControlContainer">
          <ol class="newNoteResultTodos">
            <!-- <li class="newNoteResultTodo">
                                <div class="newNoteResultSubContainer">
                                    <p class="newNoteResultItemText">At first I would like to install Windows</p><button type="button" class="newNoteBtn removeTodoBtn">Remove item</button>
                                </div>
                            </li>
                            <li class="newNoteResultTodo">
                                <div class="newNoteResultSubContainer">
                                    <p class="newNoteResultItemText">At second I need to install proper drivers</p><button type="button" class="newNoteBtn removeTodoBtn">Remove item</button>
                                </div>
                            </li>
                            <li class="newNoteResultTodo">
                                <div class="newNoteResultSubContainer">
                                    <p class="newNoteResultItemText">After that I need to install basic programs</p><button type="button" class="newNoteBtn removeTodoBtn">Remove
                                        item</button>
                                </div>
                            </li>
                            <li class="newNoteResultTodo">
                                <div class="newNoteResultSubContainer">
                                    <p class="newNoteResultItemText">Finally I can install any other programs or games - depends what I want to be installed</p><button type="button"
                                        class="newNoteBtn removeTodoBtn">Remove
                                        item</button>
                                </div>
                            </li> -->
            <li
              v-for="(task, index) in myList"
              :key="index"
              class="newNoteResultTodo"
            >
              <div class="newNoteResultSubContainer">
                <p class="newNoteResultItemText">{{ task.todo }}</p>
                <button type="button" class="newNoteBtn removeTodoBtn">
                  Remove item
                </button>
              </div>
            </li>
          </ol>
        </div>
      </div>
      <div class="newNoteResultControl">
        <button type="button" class="newNoteBtn removeNoteBtn">
          Delete note
        </button>
        <button type="submit" class="newNoteBtn saveNoteBtn">Save note</button>
      </div>
    </div>
  </form>
</template>

<script>
import ReusableInput from "./ReusableInput.vue";
export default {
  name: "NewNote",
  components: {
    ReusableInput,
  },
  data() {
    return {
      // myList: ["At first I would like to install Windows", "At second I need to install proper drivers", "After that I need to install basic programs", "Finally I can install any other programs or games - depends what I want to be installed"]
      myList: [
        {
          todo: "At first I would like to install Windows",
          id: "1a",
          isDone: false,
        },
        {
          todo: "At second I need to install proper drivers",
          id: "2a",
          isDone: false,
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
    };
  },
};
</script>

<style scoped>
@import "../styles/addNote.css";
</style>
