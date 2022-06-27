<template>
    <div>
        <TodoForm ></TodoForm>
    </div>
</template>

<script>
// import { TodoForm } from './TodoForm.vue';
import TodoForm from './TodoForm.vue';
export default {
    name: "TodoApp",
    setup() {
        return {};
    },
    components: { TodoForm }
}
</script>

<style lang="scss" scoped>

</style>