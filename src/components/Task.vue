<template>
  <div :class="[task.reminder ? 'reminder' : '', 'task']">
  <!-- If task.reminder == True, return reminder class(border-left: green) -->
  <!-- the 'task' behind is defualt to have -->
    <h3>
      {{ task.text }}
      <i @click="onDelete()" class="fas fa-times"></i>
    </h3>
    <p>{{ task.day }}</p>
  </div>
</template>

<script>
export default {
  name: "Task",
  props: {
    task: Object,
  },
};
</script>

<style scope>
.fas {
  color: red;
}
.task {
  background: #f4f4f4;
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
}
.task.reminder {
  border-left: 5px solid green;
}
.task h3 {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>