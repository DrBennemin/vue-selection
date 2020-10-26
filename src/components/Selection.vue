<template>
  <div>
    <ul>
      <li @click="addUserToList(user)" v-for="user in users" :key="user">
        {{ user }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ["users"],
  methods: {
    addUserToList(user) {
      this.users.push(user);
    },
  },
};
</script>

<style></style>
