<template>
  <div>
    <div>
      <ul>
        <li v-for="user in selectedUsers" :key="user">
          {{ user }}
        </li>
      </ul>
    </div>
    <ul>
      <li @click="addUserToList(user)" v-for="(user, key) in users" :key="key">
        {{ user }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  user: "Listitems",
  data: function() {
    return {
      users: [
        "Boris Becker",
        "Steffi Graf",
        "Karl Dall",
        "Hennes Bender",
        "Rudi Karell",
        "Axel Stein",
        "Roberto Blanko",
      ],
      selectedUsers: [],
    };
  },
  methods: {
    addUserToList(user) {
      this.selectedUsers.push(user);
    },
  },
};
</script>

<style></style>
