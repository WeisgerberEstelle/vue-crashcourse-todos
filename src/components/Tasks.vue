<template>
  <div :key="task.id" v-for="task in tasks">
    <Task :task="task" />
  </div>
</template>

<script>
import Task from "./Task";
export default {
  name: "Tasks",
  props: {
    tasks: Array,
  },
  components: {
    Task,
  },
};
</script>
<style scoped>
.task {
  background: #ffe6e6;
  margin: 10px;
  padding: 10px 20px;
  cursor: pointer;
  
}
.task.reminder {
border-left: 5px solid green ;
}
</style>
