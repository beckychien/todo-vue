<template>
	<div class="view">
		<h1>{{title}}</h1>
		<input v-model="newTodo" @keyup.enter="addData" 
		placeholder="Anything todo?" />
		<ul>
			<!-- finish這個class透過itme中isFinished屬性決定是否新增 -->
			<li v-for="item in items" 
			v-bind:class="{finish:item.isFinished}"
			@click="toggleFinish(item)">
			{{item.text}}
		</li>
	</ul>
</div>
</template>
<script>
	export default{
		name:'ToDo',
		data(){
			return{
				title:"TodoList",
				items:[],
				newTodo:''
			}
		},
		methods:{
			toggleFinish:function(item){
				item.isFinished=!item.isFinished;
			},
			addData:function(){
				this.items.push(
				{
					text:this.newTodo,
					isFinished:false	
				},
				);
				this.newTodo="";
			}
		}
	}


</script>

<style>
.view{
	width:400px;
	border:1pz solid gray;
	margin:20px auto;
}
.view .title{

}
.view ul li{
	margin:10px 0;
	list-style:none;
}
.view .finish{
	color:gray;
	text-decoration:line-through;
}
</style>