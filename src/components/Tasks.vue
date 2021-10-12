<template>
  <div :key="task.id" v-for="task in tasks"> <!--for each task create a div and put the h3 tag inside the div-->
    <Task @delete-task="$emit('delete-task', task.id)" @toggle-reminder="$emit('toggle-reminder', task.id)"  :task="task"/>
  </div>
</template>

<script>
import Task from './Task'

export default {
  name: 'Tasks',
  props: {
    tasks: Array
  },
  components: {
    Task
  },
  emits: ['delete-task', 'toggle-reminder']
}
</script>

<style scoped>

</style>