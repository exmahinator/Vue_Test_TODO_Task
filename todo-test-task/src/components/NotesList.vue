<template>
    <ul class="notesList">
        <li class="notesItem">
            <div class="notesSubCointainer notesButtons">
                <!-- <button type="button" class="notesEdit">Edit the scroll!</button>
                <button type="button" class="notesDelete">Burn it down!</button> -->
                <button type="button" class="notesBtn notesEdit">Edit</button>
                <button type="button" class="notesBtn notesDelete">Delete</button>
            </div>
            <div class="notesSubCointainer notesTask">
                <h2>Task one</h2>
                <ul>
                    <li class="notesSubItem">
                        <label>My subtask #1<input type="checkbox" disabled checked></label>
                    </li>
                    <li class="notesSubItem">
                        <label>My subtask #2<input type="checkbox" disabled></label>
                    </li>
                    <li class="notesSubItem">
                        <label>My subtask #3<input type="checkbox" disabled></label>
                    </li>
                    <li class="notesSubItem">
                        <label>My subtask #4<input type="checkbox" disabled></label>
                    </li>
                </ul>
            </div>
        </li>
        <li class="notesItem">
            <div class="notesSubCointainer notesButtons">
                <button type="button" class="notesBtn notesEdit">Edit</button>
                <button type="button" class="notesBtn notesDelete">Delete</button>
            </div>
            <div class="notesSubCointainer notesTask">
                <h2>Task two</h2>
                <ul>
                    <li class="notesSubItem">
                        <label>My subtask #1<input type="checkbox" disabled></label>
                    </li>
                    <li class="notesSubItem">
                        <label>My subtask #2<input type="checkbox" disabled></label>
                    </li>
                </ul>
            </div>
        </li>
    </ul>
</template>

<script>
export default {
    name: 'NotesList',
    // props: {
    //     msg: String
    // }
}
</script>

<style scoped>
    @import "../styles/notesStyles.css"
</style>