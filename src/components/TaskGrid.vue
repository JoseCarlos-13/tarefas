<template>
    <div class="task-grid">
       <template v-if="tasks.length">
			<Task v-for="(task, i) in tasks"
            @taskChangeState="$emit('taskChangeState', i)"
            @deletedTask="$emit('deletedTask', i)"
            :key="task.name" 
            :task="task">
				<p>{{task.name}}</p>
			</Task>
		</template>
        <p v-else>Nenhuma tarefa agendada</p>
    </div>
</template>

<script>
import TaskItem from '@/components/TaskItem'

export default {
    components:{
        'Task': TaskItem
    },
        
    props: ['tasks']
}
</script>

<style>
   .task-grid{
       display: flex;
   }
</style>


