<template>
    <div class="task" 
    :class="changeTaskState">
        <p>{{task.name}}</p>
    </div>
</template>

<script>
export default {
    props: ['task'],

    computed:{
        changeTaskState(){
            return{
                pending: this.task.pending,
                done: !this.task.pending
            }
        }
    }
}
</script>

<style>
    .task{
        border-radius: 12px;
        padding: 15px;
        background-color: darkolivegreen;
        border-right: 8px solid black;
        border-bottom: 6px solid black;
        border-top: 0px solid black;
        border-left: 0px solid black;
        color: white;
        font-size: 14pt;
        margin: 20px;
        font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
        user-select: none;
    }

    .pending{
        background-color: darkred;
        border-right-color: rgb(75, 1, 1);
        border-bottom-color: rgb(68, 7, 2);

    }

    .done{
        background-color: darkgreen;
        border-right-color: rgb(0, 41, 5);
        border-bottom-color: rgb(0, 48, 4);
    }
</style>


