<template>
    <div>
       <template>
			<div v-for="task in tasks" :key="task.name" >
				<button class="task"><p>{{task.action}}</p></button>
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
        box-shadow: 4px 8px 5px black;
        border-radius: 12px;
        padding: 15px;
        background-color: darkgreen;
        border-right: 8px solid black;
        border-bottom: 5px solid black;
        border-top: 0px solid black;
        border-left: 0px solid black;
        color: white;
        font-size: 14pt;
        margin: 20px;
        font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
    }
</style>


