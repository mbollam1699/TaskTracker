<template>
    <header>
        <h1>{{title}}</h1>
        <Button 
                :text="showAddTask ? 'Close': 'Add Task'" 
                :color="showAddTask ? 'red': 'green'" 
                @click="$emit('show-addTask')"/>
    </header>
</template>

<script>
    import Button from './Button'
    export default {
        name: "Header-view",
        components: {
            Button,
        },
        props: {
            title: String,
            showAddTask: Boolean,
             /*, OR as below*/
            //title: {
            //    type: String,
            //    default:"Hello World"
            //}
        }
    }

</script>

<style scoped>
    header{
        display:flex;
        justify-content:space-between;
        align-content:center;
        margin-bottom:20px;
    }

</style>