<template>
  <div>
    <span v-show="isVisible">
      Some name
      <button type="button" @click="hideUser">x</button>
    </span>
    <ul>
      <li @click="addUserToList(user)" v-for="user in users" :key="user">
        {{ user }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "SelectedUsers",
  props: ["selectedusers"],
  data() {
    return {
      isVisible: true,
    };
  },
  methods: {
    hideUser() {
      this.isVisible = false;
    },
    addUserToList(user) {
      this.selectedUsers.push(user);
    },
  },
};
</script>

<style></style>
