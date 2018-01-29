<template>
	<div>
		<div class="completed-status">
			<p>Completed Tasks: {{todos.filter(todo => { return todo.complete === true }).length }}</p>
			<p>Incomplete Tasks: {{todos.filter(todo => { return todo.complete === false }).length }}</p>
			<todo v-for="todo in todos" v-bind:todo="todo"></todo>
		</div>
	</div>
</template>

<script type=" text/javascript">

	import Todo from './Todo'

	export default {
		props: ['todos'],
		components: {
			Todo,
		},
	};

</script>		

<style>
	.completed-status {
		padding: 5px;
		border: 0.5px solid lightgray;
		width: 300px;
		margin: 20px auto;
		border-radius: 5px ;
	}
</style>