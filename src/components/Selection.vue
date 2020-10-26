<template>
  <div>
    <ul>
      <li @click="addUserToList(user)" v-for="(user, key) in users" :key="key">
        {{ user }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ["users", "selectedUsers"],
  methods: {
    addUserToList(user) {
      this.selectedUsers.push(user);
    },
  },
};
</script>
