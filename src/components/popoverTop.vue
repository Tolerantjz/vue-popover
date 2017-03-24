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
	name:'popoverTop',
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
	right: 85px;
	top: 68px;
	border-left: 10px solid transparent;
	border-top: 10px solid lightgray;
	border-bottom: 10px solid transparent;
	border-right: 10px solid transparent;
}
</style>
