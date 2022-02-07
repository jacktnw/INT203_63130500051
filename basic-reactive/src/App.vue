<script setup>
import { ref } from "vue";
const myNotes = ref([]);

const newNote = ref("");
const addNote = () => myNotes.value.push(newNote.value);
// const filNote = () => myNotes.value.filter(newNote.value);

const filter = ref();
function search() {
  const w = document.getElementsByTagName("li");
  for (let index = 0; index < w.length; index++) {
    let y = w[index].textContent;
    if (y.indexOf(filter.value) > -1) {
      w[index].style.display = "";
    } else {
      w[index].style.display = "none";
    }
  }
}
</script>

<template>
  <div v-show="myNotes != 0">
    <label>Filter Note: </label>
    <input type="text" id="filter" v-model="filter" @keyup="search" />
  </div>

  <div>
    <ul>
      <li v-for="(note, index) in myNotes">
        {{ note }}
      </li>
    </ul>
  </div>

  <div>
    <label>New Note: </label>
    <input type="text" v-model="newNote" />
    <button @click="addNote" style="cursor: pointer">Add Note</button>
  </div>
</template>

<style></style>
