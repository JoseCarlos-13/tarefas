<template>
	<div id="app">
		<h1>Tarefas</h1>
		<tasks-grid/>
	</div>
</template>

<script>
import Tasks from './components/TaskGrid'
export default {
	components: {
		'tasks-grid': Tasks
	},
	props: ['tasks']
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
