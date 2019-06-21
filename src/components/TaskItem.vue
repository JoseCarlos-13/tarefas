<template>
    <div class="task" 
    :class="changeTaskState">
        <span class="close">x</span>
        <p>{{task.name}}</p>
    </div>
</template>

<script>
export default {
    props: ['task'],

    computed:{
        changeTaskState(){
            return{
                done: this.task.pending,
                pending: !this.task.pending
            }
        }
    }
}
</script>

<style>
    .task{
        border-radius: 12px;
        padding: 35px;
        background-color: darkolivegreen;
        border-right: 8px solid black;
        border-bottom: 6px solid black;
        color: white;
        padding-right: 55px;
        font-size: 14pt;
        margin: 20px;
        display: flex;
        justify-content: center;
        align-items: center;
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

    .close {
        background-color: rgba(255, 250, 240, 0.219);
        color: rgb(255, 255, 255);
        display: flex;
        justify-content: center;
        position: relative;
        top: -45px;
        right: 25px;
        padding-left: 8px;
        padding-right: 8px;
        padding-bottom: 2px;
        border-radius: 35px;
    }

    .pending .close{
        background-color: rgba(214, 4, 4, 0.548);
    }

    .done .close{
        background-color: rgba(1, 161, 1, 0.418);
    }
</style>


