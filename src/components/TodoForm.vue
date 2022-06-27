<!-- TodoForm.vue -->
<template>
    <form @submit.prevent="addItemAndClear(todo)">
        <input v-model="todo" type="text">
        <button>Add</button>
    </form>
</template>

<script>
import { ref } from 'vue'
import { useTodoListStore } from '@/store/useTodoListStore';

export default {
  name: 'TodoForm',
    setup () {
        const todo = ref("");
        // use Pinia store:
        const store = useTodoListStore()

        function addItemAndClear(item) {
            if(item.length === 0) {
                return
            }
            // invokes function in the store:
            store.addTodo(item)
            todo.value = ''
        }

        return { todo };
    },
};
</script>

<style lang="scss" scoped>

</style>