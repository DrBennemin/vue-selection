<template>
  <div>
    <span v-show="isVisible">
      Some name
      <button type="button" @click="hideUser">x</button>
    </span>
  </div>
</template>

<script>
export default {
  name: "Selection",
  data() {
    return {
      isVisible: true,
    };
  },
  methods: {
    hideUser() {
      this.isVisible = false;
    },
  },
};
</script>

<style></style>
