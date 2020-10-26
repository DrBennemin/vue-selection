<template>
  <div id="app">
    <SelectedUsers :selected-users="selectedUsers" />
    <Selection :users="users" :selected-users="selectedUsers" />
  </div>
</template>

<script>
import Selection from "./components/Selection";
import SelectedUsers from "./components/SelectedUsers";

export default {
  components: {
    Selection,
    SelectedUsers,
  },
  data: function() {
    return {
      selectedUsers: [],
      users: [
        "Boris Becker",
        "Steffi Graf",
        "Karl Dall",
        "Hennes Bender",
        "Rudi Karell",
        "Axel Stein",
        "Roberto Blanko",
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  text-align: left;
}
</style>
