<template>
	<div id="app">
		<h1>Tarefas</h1>
		<add-task @addItem="addOneTask"/>
		<task-grid :tasks="tasks"/>
	</div>
</template>

<script>
import TaskList from '@/components/TaskGrid'
import AddTask from '@/components/addTask'

export default {
	components: {
		'task-grid': TaskList,
		'add-task': AddTask
	},

	data () {
        return{
            tasks: [
                { name: "run in the street", pending: false},
            ]
        }
	},
	
	methods: {
		addOneTask(task){
			const sameName = t => t.name === task.name
			const reallyNew = this.tasks.filter(sameName).length == 0
			if (reallyNew) {
				this.tasks.push({
					name: task.name,
					pending: task.pending || false
				})
			}
		}
	}
}
</script>

<style>
	body {
		font-family: Georgia, 'Times New Roman', Times, serif;
		background: linear-gradient(to right, rgb(16, 31, 19), rgb(36, 77, 68));
		color: rgb(255, 255, 255);
	}

	#app {
		display: flex;
		flex: 1;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}

	#app h1 {
		margin-bottom: 5px;
		font-weight: 300;
		font-size: 4rem;
	}
</style>
