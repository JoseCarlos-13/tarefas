<template>
    <div>
        <input class="addTask" v-model="taskName" @keyup.enter="add" type="text"/>
        <button @click="add" class="addBtn" type="primary">+</button>
    </div>
</template>

<script>
export default {
    props: ['tasks'],

    data () {
        return {
            taskName: ''
        }
    },

    methods: {
        add () {
            this.$emit("addItem", { name: this.taskName })
            this.taskName = ''
        }
    }
}
</script>

<style>
    .addTask{
        padding: 10px;
        border-radius: 5px;
        width: 450px;
        color: white;
        border-color: rgb(255, 255, 255);
        margin-bottom: 40px;
        margin-top: 50px;
        background-color: rgba(2, 255, 179, 0.212);
    }

    .addBtn{
        padding: 10px;
        width: 35px;
        background-color: rgba(2, 255, 179, 0.212);
        color: white;
        border-radius: 5px; 
    }
</style>
