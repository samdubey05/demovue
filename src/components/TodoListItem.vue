<script>
export default {
    name: 'TodoListItem',
    props: {
        todo: {
            type: Object,
            required: true
        }
    }
}
</script>

<template>
  <li>
      <span>{{ todo.text }}</span>
  </li>
</template>

<style>

</style>