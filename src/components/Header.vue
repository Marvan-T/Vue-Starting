<template>
  <h1>{{title}}</h1>
  <Button @btn-click="this.$emit('show-add-task')" :text="showAddTask ? 'Close' : 'Add Task'" :color="showAddTask ? 'Red' : 'Green '"/>
</template>

<script>
import Button from './Button'
export default {
  name: 'Header',
  props: {
    title: String,
    showAddTask: Boolean
  },
  components: {
    Button
  },
  emits: ['show-add-task']
}

</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>