<template>
    <div>
       <template>
			<div v-for="task in tasks" :key="task.name">
				<p>{{task.name}}</p>
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

</style>


