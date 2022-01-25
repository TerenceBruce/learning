<!-- Fix the errors! -->
<template>
<div>
  <!-- Make this h2 element appear on the web page -->
  <h2>{{ full_name }}</h2>
  <input type="text" placeholder="First Name" @input=??? />
  <input type="text" placeholder="Last Name" @input=??? />
  <button ?click=???>Change Code Editor</button>
</div>
</template>

<script>
import { ?, ?, ? } from "vue";

export default {
  setup() {
    // Shared
    const first_name = ref("");
    const last_name = ref("");
    const editor = ref("");

    function setFirstName(event) {
      first_name.? = event.target.value;
    }

    function setLastName(event) {
      last_name.? = event.target.value;
    }

    function changeEditor() {
      editor.value = "Notepad";
    }

    const fullName = computed( () => {
      return first_name.value + " " + last_name.value;
    });

    watch(editor, (?, ?) => {
      console.log("Previous Editor: " + oldValue);
      console.log("New Editor: " + newValue);
    })

    return { ?, ?, ?, ? }
  }
};
</script>

<style>

</style>