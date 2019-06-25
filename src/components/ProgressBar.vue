<template>
        <div class="tasks-progress">
            <span class="bar">{{progressBar}}%</span>
            <div class="progress-bar" :style="{width: progressBar + '%'}"></div>
        </div>
</template>

<script>
export default {
    props: {
        progressBar: {type: Number, default: 0}
    }
}
</script>

<style>
    .tasks-progress{
        border: 1px solid white;
        width: 80%;
        color: white;
        border-radius: 5px;
        position: relative;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .progress-bar{
        background-color: green;
        height: 100%;
        display: flex;
        position: absolute;
        align-self: flex-start;
    }

    .bar{
        z-index: 1;
    }
</style>



