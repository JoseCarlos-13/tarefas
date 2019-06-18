<template>
    <div>
       <template>
			<div v-for="task in tasks" :key="task.name" class="task">
				<p>{{task.action}}</p>
			</div>
		</template>
    </div>
</template>

<script>

export default {
    data () {
        return{
            tasks: [
                { name: "Race", action: "run in the street"},
                { name: "Cook", action: "cook a dinner"}
            ]
        }
    }
}
</script>

<style>
    .task{
        box-shadow: 4px 8px 2px black;
        border-radius: 8px;
        padding: 15px;
        background-color: darkgreen;
        border-right: 5px solid black;
        font-size: 14pt;
        margin: 20px;
        font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
    }
</style>


