<template>
	<div class="ui centered card">
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
		<!-- if the todo is completed show -->
		<div class="ui bottom attached green basic button" v-show="todo.complete">Completed</div>
		<!-- if the todo is not completed show -->
    <div class='ui bottom attached red basic button' v-show="!todo.complete">Complete</div>
	</div>
</template>

<script type="text/javascript">
	
	export default {
		props: ['todos']
	};

</script>