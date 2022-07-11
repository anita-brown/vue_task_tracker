<template>
  <header>
    <h1>
      {{title}}
    </h1>
    <Button @show-add-task="$emit('show-add-task')" :text="showAddTask ? 'Close' : 'Add Task'" color="green"/>
  </header>
</template>

<script>
import Button from './Button.vue'
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Header',
  components: {
    Button
  },
  props: {
    title: String,
    showAddTask: Boolean
  }

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
