<template>
	<div class="parent">
		<div class="content">
			{{content}}
		</div>
		<div class="triangle"></div>
	</div>
</template>
<script>
export default{
	name:'popoverLeft',
	data(){
		return {
			
		}
	},
	props:{
		content:String
	}
}
</script>
<style scoped>
.parent{position: relative;}
.content{
	background-color: white;
	border:1px solid lightgray;
	position: absolute;
	padding: 5px 10px;
	border-radius: 5px;
}
.triangle{
	position: absolute;
	right: -20px;
	top: 25px;
	border-left: 10px solid lightgray;
	border-top: 10px solid transparent;
	border-bottom: 10px solid transparent;
	border-right: 10px solid transparent;
}
</style>
