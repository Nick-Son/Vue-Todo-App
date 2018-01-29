<template>
	<div>
		<div class="completed-status">
			<p>Completed Tasks: {{todos.filter(todo => { return todo.complete === true }).length }}</p>
			<p>Incomplete Tasks: {{todos.filter(todo => { return todo.complete === false }).length }}</p>
		</div>

		<div class="ui centered card" v-for="todo in todos">
			<div class="content">
				<div class="header">
					{{todo.title}}
				</div>
				<div class="meta">
					{{todo.project}}
				</div>
				<div class="extra content">
					<span class='right float edit icon'>
						<i class="edit icon"></i>
					</span>
				</div>	
			</div>
		</div>
	</div>
</template>

<script type=" text/javascript">
	export default {
		props: ['todos'],
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