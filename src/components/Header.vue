<template>
    <header>
        <h1>{{ title }}</h1>
        <div v-if="showAddTask">
            <Button @btn-click="$emit('toggle-add-task')" text="Close" color="red" />
        </div>
        <div v-else>
            <Button @btn-click="$emit('toggle-add-task')" text="Add Task" color="green" />
        </div>
    </header>
</template>

<script>
import Button from './Button.vue'

    export default {
        name: 'Header',
        props: {
            title: String,
            showAddTask: Boolean,
        },
        components: {
            Button,
        },
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