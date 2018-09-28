<template>
	<div class="headerview">
		<h1>{{msg}}</h1>
	</div>
</template>>


<script>
	export default{
		data(){
			return{
				title:"I'm title!!!"
			}
		},
		//父組件傳遞給子組件,
		props:{
			msg:{	//自定義屬性
				type:String,
				default:"default title"
			}
		}
	}
</script>

<style>
</style>