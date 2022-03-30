<template>
  <header>
    <h1>{{ title }}</h1>
    <HeaderButton
      @toggle-add-task="$emit('toggle-add-task')"
      :text="showAddTask ? 'Close' : 'Add Task'"
      :color="showAddTask ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import HeaderButton from "./Button.vue";
export default {
  name: "Header-component",
  props: ["title", "showAddTask"],
  components: {
    HeaderButton,
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>