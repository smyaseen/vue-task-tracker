<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      @onClick="$emit('toggle-show-add-task')"
      :text="buttonText"
      :color="showAddTask ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import Button from "./Button";

export default {
  name: "Header",
  props: {
    title: String,
    buttonText: String,
    showAddTask: Boolean,
  },
  components: {
    Button,
  },
  emits: ["toggle-show-add-task"],
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
