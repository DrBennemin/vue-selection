<template>
  <div v-show="isVisible">
    <span v-for="(user, key) in selectedUsers" :key="key">
      {{ user }}
      <button type="button" @click="isVisible = false">x</button>
    </span>
  </div>
</template>

<script>
export default {
  props: ["selectedUsers"],
  data() {
    return {
      isVisible: true,
    };
  },
};
</script>
