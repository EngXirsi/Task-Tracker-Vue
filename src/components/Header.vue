<template>
    <header>
        <h1>{{title}}</h1>
        <Button @toggle-add-task = "$emit('toggle-add-task')"  :text="showAddTask ? 'Close Task' : 'Add Task' " 
        :color = "showAddTask ? 'red' : 'green' "/>
        
    </header>
</template>

<script>
import Button from './Button.vue'
export default {
    name: "Header",
    props: {
        title: String,
        showAddTask : Boolean
    },
    components:{
        Button
    },
    methods: {
     
    }
    
}
</script>
<style scoped>
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 20px;
}
</style>