<template>
    <div>
        <input class="addTask" type="text"/><button class="addBtn">+</button>
    </div>
</template>

<script>
export default {
    props: ['tasks']
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
    }
</style>
