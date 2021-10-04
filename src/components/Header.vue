<template>
    <header>
        <h1>{{ title }}</h1>
        <Button :text="showAddTask ? 'Close' : 'Add Task'" :color="showAddTask ? 'darkred' : 'darkgreen'" @btn-click="$emit('form-toggle')" />
    </header>
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
    emits: ['form-toggle']
}
</script>

<style scoped>
header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}
</style>
