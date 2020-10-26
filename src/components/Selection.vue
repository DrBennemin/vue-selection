<template>
  <div>
    <div>
      <ul>
        <li v-for="user in users" :key="user">
          {{ user }}
        </li>
      </ul>
    </div>
    <!-- <ul>
      <li @click="addUserToList(user)" v-for="(user, key) in users" :key="key">
        {{ user }}
      </li>
    </ul> -->
  </div>
</template>

<script>
export default {
  props: ["users"],
  methods: {
    addUserToList(user) {
      this.selectedUsers.push(user);
    },
  },
};
</script>

<style></style>
