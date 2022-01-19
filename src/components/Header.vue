<template>
    <header>
        <h1>{{title}}</h1>
        <Button
            @btn-click="$emit('toggel-add-task')"
            :color="ShowAddTask ?'red':'green'" 
            :text="ShowAddTask ? 'Close':'Add task'"
        />
    </header>
</template>
<script>
import Button from './Button.vue'
export default {
    name:"Header",
    props:{
        title:String,
        ShowAddTask :Boolean
    },
    components:{
        Button,
    },
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