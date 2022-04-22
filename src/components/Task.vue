<template>
  <div @dblclick="$emit('toggle-reminder', task.id)" :class="[task.reminder ? 'reminder' : '', 'task']">
    <h3>
      {{ task.text }}
      <i @click="$emit('delete-task', task.id)" class="bi bi-trash3-fill trash"></i>
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
  methods:{
    onDelete(id){
      this.$emit('delete-task', id )
    },
  }
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
.task h3 {
  display:flex;
  justify-content: space-between;
}
.trash{
  color:red;
}
</style>
