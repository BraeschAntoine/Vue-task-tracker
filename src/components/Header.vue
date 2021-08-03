<template>
    <header>
        <h1> {{ title }} </h1>
        <Button @button-clicked="$emit('button-clicked')" :text="showAddTask ? 'Close' : 'Add Task'" :color="showAddTask ? 'green' : 'red'"/>
    </header>
</template>

<script>
import Button from './Button'

    export default {
        name: 'Header',
        components: {
            Button
        },
        props: {
            title: {
                type: String,
                default: 'Header Component'
            },
            showAddTask: Boolean
        },
        emits: ['button-clicked']
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