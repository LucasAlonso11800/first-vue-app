<template>
  <header>
    <h1>{{ title }}</h1>
    <HeaderButton text="Add Task" color="green"/>
  </header>
</template>

<script>
import HeaderButton from './Button.vue'; 
export default {
  name: "Header-component",
  props: ["title"],
  components: {
      HeaderButton
  }
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