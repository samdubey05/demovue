<script>
import BaseInputText from '@/components/BaseInputText'
import TodoListItem from '@/components/TodoListItem'
export default {
    name: 'TodoList',
    components: {
        BaseInputText,
        TodoListItem
    },
    data () {
        return {
            todos: [
              {
                text: 'test'
              }
            ],
            todoText: ''
        }
    },
    methods: {
        addTodo (value) {
            this.todos.push({
                text: value
            })
            console.log('Hello', value)
        }
    }
}
</script>

<template>
  <div>
    <BaseInputText :fromPropValue="todoText" @inputtext="addTodo" />
    <TodoListItem v-for="todo in todos" :key="todo.text" :todo="todo"/>
  </div>
</template>

<style>

</style>